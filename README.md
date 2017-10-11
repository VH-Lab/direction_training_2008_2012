# direction_training_2008_2012
Before and after direction responses (Li/Van Hooser et al. 2008; Van Hooser/Li/Christensson et al. 2012)

These are large saved analysis records from Li/Van Hooser et al. 2008 (bidirectional training) and Van Hooser/Li/Vhristensson et al. 2012 (unidirectional training). The files have many variables, some of which are unimportant (such as looping variables). But the following variables have useful information in the form of a cell list. It is okay if you get errors on warning, those fields are not critical.

Variable (description)
 -DI: Direction index ( (pref-null)/pref )
 -OI: Orientation index ( (pref-orth)/pref )
 -DIbr: Direction index, blank rectified (used in the papers)  ( min(1,(pref-null)/(pref-blank)) )
 -OIbr: Orientation index, blank rectified (used in the papers ( min(1,(pref-orth)/(pref-blank)) )
 -tdi: Direction index in the trained direction (used in 2012 paper) ( R(trained_dir)/(R(trained_dir)+R(trained_dir+180)) )
 -pref: Response in the preferred direction
 -null: Response in the null direction
 -orth: Response in the orthogonal orientation
 -cellnamevar: the name of each cell
 -experindex: the experiment from which each cell is drawn
 
 Each of the above variables are in a cell list with an index. The index represents the type of direction tuning data it holds:
    1=naive (all naive responses)
    2=motion (responses from animals after trainining with motion)
    3=flash (responses from animals after training with flash)
    4=experienced (responses from animals that are experienced)
    5=naive_responly (cells that exhibited significant responses for the naive condition only but were missing or unresponsive later)
    6=motion_responly (cells that exhibited responses after motion training but that were missing or unresponsive earlier),
    7=flash_responly (cells that exhibited responses after flash training but that were missing or unresponsive earlier),
    8=naive_presentonly (cells that were only present in the naive case)
    9=motion_presentonly (cells that were only present after motion training)
    10=flash_presentonly (cells that were only present after flash training)
    11=naive_flash (naive responses from animals trained with flash)
    12=naive w/ motion or flash, (naive responses from animals trained with flash or motion)
    13=motion w/naive (motion-trained cells that had a response in the naive condition)
    14=flash w/ naive (flash-trained cells that had a response in the naive condition)

For example:

z = load('bidirectional_variables.mat');
z.DIbr{1} % all cells that exhibited responses in the naive conditions

