# hoangmanhdatofficial.github.io
Hoc tieng anh
cat > /tmp/build_vocab.py << 'PYEOF'
# Compile all vocabulary into structured JSON-like format for embedding in HTML

vocab_data = {
    "units": [
        {
            "id": 1,
            "name": "The Natural World",
            "color": "#2d6a4f",
            "topics": [
                {
                    "name": "Environmental Impacts of Logging",
                    "words": [
                        {"word": "aquatic", "pos": "adj.", "meaning": "Sống trong nước; liên quan đến nước", "example": "Many aquatic animals are endangered due to deforestation.", "ipa": "/əˈkwætɪk/"},
                        {"word": "array", "pos": "n.", "meaning": "Một số lượng lớn, bộ sưu tập", "example": "The logging industry supplies an array of products.", "ipa": "/əˈreɪ/"},
                        {"word": "defense", "pos": "n.", "meaning": "Sự bảo vệ, phòng thủ", "example": "Trees provide a natural defense against air pollution.", "ipa": "/dɪˈfens/"},
                        {"word": "deforestation", "pos": "n.", "meaning": "Sự phá rừng, chặt phá cây trên diện rộng", "example": "Deforestation impacts rainfall patterns significantly.", "ipa": "/ˌdiːˌfɒrɪˈsteɪʃn/"},
                        {"word": "environment", "pos": "n.", "meaning": "Môi trường tự nhiên", "example": "Logging causes untold harm to the environment.", "ipa": "/ɪnˈvaɪrənmənt/"},
                        {"word": "erosion", "pos": "n.", "meaning": "Sự xói mòn đất do nước hoặc gió", "example": "Tree roots help prevent erosion.", "ipa": "/ɪˈroʊʒn/"},
                        {"word": "extend", "pos": "v.", "meaning": "Vươn ra, mở rộng, kéo dài", "example": "The effects of logging extend beyond just the felling of trees.", "ipa": "/ɪkˈstend/"},
                        {"word": "fell", "pos": "v.", "meaning": "Chặt hạ (cây)", "example": "Loggers fell hundreds of trees every day.", "ipa": "/fel/"},
                        {"word": "habitat", "pos": "n.", "meaning": "Môi trường sống tự nhiên của động thực vật", "example": "Many animals lose their habitat due to deforestation.", "ipa": "/ˈhæbɪtæt/"},
                        {"word": "impact", "pos": "n.", "meaning": "Tác động mạnh, ảnh hưởng lớn", "example": "The impact of logging on the environment is severe.", "ipa": "/ˈɪmpækt/"},
                        {"word": "inhibit", "pos": "v.", "meaning": "Ngăn chặn, làm chậm lại", "example": "Tree shade inhibits the growth of algae.", "ipa": "/ɪnˈhɪbɪt/"},
                        {"word": "intercept", "pos": "v.", "meaning": "Chặn bắt, ngăn chặn", "example": "The canopy intercepts heavy rainfall.", "ipa": "/ˌɪntəˈsept/"},
                        {"word": "logging", "pos": "n.", "meaning": "Hoạt động khai thác gỗ thương mại", "example": "Logging is a major cause of deforestation.", "ipa": "/ˈlɒɡɪŋ/"},
                        {"word": "myriad", "pos": "adj.", "meaning": "Vô số, rất nhiều", "example": "The rain forest is home to myriad plant life.", "ipa": "/ˈmɪriəd/"},
                        {"word": "nutrient", "pos": "n.", "meaning": "Chất dinh dưỡng", "example": "Trees provide nutrients for the ecosystem.", "ipa": "/ˈnjuːtriənt/"},
                        {"word": "pollution", "pos": "n.", "meaning": "Ô nhiễm không khí, nước, v.v.", "example": "Trees provide a natural defense against air pollution.", "ipa": "/pəˈluːʃn/"},
                        {"word": "stabilize", "pos": "v.", "meaning": "Ổn định, duy trì không thay đổi", "example": "Tree roots stabilize the soil.", "ipa": "/ˈsteɪbɪlaɪz/"},
                        {"word": "terrestrial", "pos": "adj.", "meaning": "Sống trên cạn, liên quan đến đất liền", "example": "Both terrestrial and aquatic animals are affected.", "ipa": "/təˈrestriəl/"},
                        {"word": "vanish", "pos": "v.", "meaning": "Biến mất", "example": "Many life forms vanish as forests disappear.", "ipa": "/ˈvænɪʃ/"},
                        {"word": "vegetation", "pos": "n.", "meaning": "Thực vật, cây cối", "example": "Vegetation along rivers helps maintain water flow.", "ipa": "/ˌvedʒɪˈteɪʃn/"}
                    ]
                },
                {
                    "name": "Bird Migration",
                    "words": [
                        {"word": "aspect", "pos": "n.", "meaning": "Khía cạnh, đặc điểm", "example": "Migration is a fascinating aspect of bird behavior.", "ipa": "/ˈæspekt/"},
                        {"word": "breed", "pos": "v.", "meaning": "Sinh sản, nhân giống", "example": "Birds breed in warmer climates.", "ipa": "/briːd/"},
                        {"word": "diurnal", "pos": "adj.", "meaning": "Hoạt động ban ngày", "example": "Diurnal birds are active during daylight hours.", "ipa": "/daɪˈɜːrnl/"},
                        {"word": "endure", "pos": "v.", "meaning": "Chịu đựng điều kiện khó khăn", "example": "Migrating birds endure extreme weather conditions.", "ipa": "/ɪnˈdjʊər/"},
                        {"word": "evolve", "pos": "v.", "meaning": "Phát triển dần dần, tiến hóa", "example": "Birds have evolved remarkable navigation abilities.", "ipa": "/ɪˈvɒlv/"},
                        {"word": "fascinate", "pos": "v.", "meaning": "Hấp dẫn, thu hút sự chú ý mạnh mẽ", "example": "Bird migration fascinates scientists worldwide.", "ipa": "/ˈfæsɪneɪt/"},
                        {"word": "feat", "pos": "n.", "meaning": "Thành tích, kỳ công khó khăn", "example": "Migration is an incredible feat of endurance.", "ipa": "/fiːt/"},
                        {"word": "fuel", "pos": "v.", "meaning": "Cung cấp năng lượng", "example": "Fat reserves fuel birds during long migrations.", "ipa": "/fjuːəl/"},
                        {"word": "hemisphere", "pos": "n.", "meaning": "Bán cầu trái đất", "example": "Birds migrate between hemispheres.", "ipa": "/ˈhemɪsfɪər/"},
                        {"word": "imperative", "pos": "n.", "meaning": "Điều cấp bách, ưu tiên", "example": "Finding food is an imperative for migrating birds.", "ipa": "/ɪmˈperətɪv/"},
                        {"word": "inhabit", "pos": "v.", "meaning": "Sinh sống ở, cư trú tại", "example": "These birds inhabit tropical regions.", "ipa": "/ɪnˈhæbɪt/"},
                        {"word": "migration", "pos": "n.", "meaning": "Sự di cư từ nơi này sang nơi khác", "example": "Bird migration is one of nature's greatest spectacles.", "ipa": "/maɪˈɡreɪʃn/"},
                        {"word": "navigation", "pos": "n.", "meaning": "Việc tìm đường từ nơi này sang nơi khác", "example": "Birds use stars for navigation.", "ipa": "/ˌnævɪˈɡeɪʃn/"},
                        {"word": "nocturnal", "pos": "adj.", "meaning": "Hoạt động ban đêm", "example": "Owls are nocturnal birds.", "ipa": "/nɒkˈtɜːrnl/"},
                        {"word": "observer", "pos": "n.", "meaning": "Người quan sát", "example": "Bird observers track migration patterns.", "ipa": "/əbˈzɜːrvər/"},
                        {"word": "obscure", "pos": "v.", "meaning": "Làm khó nhìn thấy, che khuất", "example": "Clouds obscure the stars used for navigation.", "ipa": "/əbˈskjʊər/"},
                        {"word": "optimal", "pos": "adj.", "meaning": "Tốt nhất, thuận lợi nhất", "example": "Birds seek optimal weather conditions for migration.", "ipa": "/ˈɒptɪməl/"},
                        {"word": "species", "pos": "n.", "meaning": "Loài sinh vật", "example": "Many species of birds migrate annually.", "ipa": "/ˈspiːʃiːz/"},
                        {"word": "stray", "pos": "v.", "meaning": "Lạc đường, tách khỏi đàn", "example": "Young birds sometimes stray from the flock.", "ipa": "/streɪ/"},
                        {"word": "windswept", "pos": "adj.", "meaning": "Không được che chắn khỏi gió", "example": "Birds struggle in windswept conditions.", "ipa": "/ˈwɪndswept/"}
                    ]
                },
                {
                    "name": "Plant Life in the Taklimakan Desert",
                    "words": [
                        {"word": "accumulate", "pos": "v.", "meaning": "Tích lũy dần theo thời gian", "example": "Sand dunes accumulate over centuries.", "ipa": "/əˈkjuːmjəleɪt/"},
                        {"word": "adapt", "pos": "v.", "meaning": "Thích nghi với hoàn cảnh", "example": "Desert plants adapt to survive without much water.", "ipa": "/əˈdæpt/"},
                        {"word": "determine", "pos": "v.", "meaning": "Quyết định, xác định", "example": "Scientists determine which plants can survive the desert.", "ipa": "/dɪˈtɜːrmɪn/"},
                        {"word": "dilute", "pos": "v.", "meaning": "Pha loãng, làm yếu đi bằng cách trộn với nước", "example": "Rain dilutes the salt in desert soil.", "ipa": "/daɪˈluːt/"},
                        {"word": "diverse", "pos": "adj.", "meaning": "Đa dạng, nhiều loại khác nhau", "example": "The desert has a diverse range of plant adaptations.", "ipa": "/daɪˈvɜːrs/"},
                        {"word": "evaporation", "pos": "n.", "meaning": "Sự bay hơi, mất nước vào không khí", "example": "High evaporation rates make deserts very dry.", "ipa": "/ɪˌvæpəˈreɪʃn/"},
                        {"word": "extreme", "pos": "adj.", "meaning": "Khắc nghiệt, rất dữ dội", "example": "Desert plants tolerate extreme temperatures.", "ipa": "/ɪkˈstriːm/"},
                        {"word": "fringe", "pos": "n.", "meaning": "Rìa, mép của cái gì đó", "example": "Plants grow on the fringe of the desert.", "ipa": "/frɪndʒ/"},
                        {"word": "mechanism", "pos": "n.", "meaning": "Cơ chế, hành vi đối phó với tình huống khó", "example": "Plants have unique mechanisms to store water.", "ipa": "/ˈmekənɪzəm/"},
                        {"word": "minimize", "pos": "v.", "meaning": "Giảm thiểu đến mức thấp nhất", "example": "Desert plants minimize water loss.", "ipa": "/ˈmɪnɪmaɪz/"},
                        {"word": "moisture", "pos": "n.", "meaning": "Độ ẩm, hơi nước", "example": "Desert plants absorb moisture from the air.", "ipa": "/ˈmɔɪstʃər/"},
                        {"word": "occupy", "pos": "v.", "meaning": "Tồn tại ở một nơi, sinh sống tại", "example": "Few plants occupy the central desert.", "ipa": "/ˈɒkjəpaɪ/"},
                        {"word": "prolific", "pos": "adj.", "meaning": "Sản xuất nhiều", "example": "Some desert plants are prolific seed producers.", "ipa": "/prəˈlɪfɪk/"},
                        {"word": "resilient", "pos": "adj.", "meaning": "Kiên cường, chịu đựng được điều kiện khó khăn", "example": "Desert plants are remarkably resilient.", "ipa": "/rɪˈzɪliənt/"},
                        {"word": "sparse", "pos": "adj.", "meaning": "Thưa thớt, ít ỏi", "example": "Vegetation is sparse in the Taklimakan Desert.", "ipa": "/spɑːrs/"},
                        {"word": "stressor", "pos": "n.", "meaning": "Yếu tố gây khó khăn lớn", "example": "Heat is a major stressor for desert plants.", "ipa": "/ˈstresər/"},
                        {"word": "swing", "pos": "n.", "meaning": "Sự thay đổi đột ngột, lớn", "example": "Temperature swings in the desert can be extreme.", "ipa": "/swɪŋ/"},
                        {"word": "thrive", "pos": "v.", "meaning": "Phát triển tốt, sinh trưởng mạnh", "example": "Only tough plants thrive in the desert.", "ipa": "/θraɪv/"},
                        {"word": "transitional", "pos": "adj.", "meaning": "Liên quan đến sự thay đổi từ loại này sang loại khác", "example": "The desert fringe is a transitional zone.", "ipa": "/trænˈzɪʃənl/"},
                        {"word": "violent", "pos": "adj.", "meaning": "Mạnh mẽ, đột ngột và phá hoại", "example": "Violent sandstorms are common in the desert.", "ipa": "/ˈvaɪələnt/"}
                    ]
                }
            ]
        },
        {
            "id": 2,
            "name": "Leisure Time",
            "color": "#1b4332",
            "topics": [
                {
                    "name": "Peripheral Vision in Sports",
                    "words": [
                        {"word": "anticipate", "pos": "v.", "meaning": "Dự đoán, sẵn sàng cho điều gì đó xảy ra", "example": "Athletes anticipate their opponent's next move.", "ipa": "/ænˈtɪsɪpeɪt/"},
                        {"word": "athlete", "pos": "n.", "meaning": "Vận động viên thể thao", "example": "Professional athletes train their peripheral vision.", "ipa": "/ˈæθliːt/"},
                        {"word": "blur", "pos": "n.", "meaning": "Hình ảnh mờ nhạt, không rõ ràng", "example": "Fast movements appear as a blur.", "ipa": "/blɜːr/"},
                        {"word": "boundary", "pos": "n.", "meaning": "Đường biên, ranh giới", "example": "Athletes must stay within the boundary.", "ipa": "/ˈbaʊndri/"},
                        {"word": "complicate", "pos": "v.", "meaning": "Làm phức tạp thêm", "example": "Crowd noise can complicate an athlete's focus.", "ipa": "/ˈkɒmplɪkeɪt/"},
                        {"word": "coordinate", "pos": "v.", "meaning": "Phối hợp, làm việc nhịp nhàng với nhau", "example": "Athletes coordinate hand and eye movements.", "ipa": "/kəʊˈɔːrdɪneɪt/"},
                        {"word": "demonstrate", "pos": "v.", "meaning": "Trình diễn, thể hiện", "example": "Coaches demonstrate correct techniques.", "ipa": "/ˈdemənstreɪt/"},
                        {"word": "detect", "pos": "v.", "meaning": "Nhận ra, phát hiện", "example": "Athletes detect movement using peripheral vision.", "ipa": "/dɪˈtekt/"},
                        {"word": "distracting", "pos": "adj.", "meaning": "Gây phân tâm, làm mất tập trung", "example": "Crowd noise is distracting to players.", "ipa": "/dɪˈstræktɪŋ/"},
                        {"word": "focus", "pos": "v.", "meaning": "Tập trung vào một vật thể", "example": "Athletes focus on the ball at all times.", "ipa": "/ˈfoʊkəs/"},
                        {"word": "indiscernibly", "pos": "adv.", "meaning": "Theo cách không thể nhìn thấy hay nhận biết", "example": "The puck moves almost indiscernibly fast.", "ipa": "/ˌɪndɪˈsɜːrnəbli/"},
                        {"word": "indistinct", "pos": "adj.", "meaning": "Không rõ ràng, mờ nhạt", "example": "Fast objects appear indistinct to the eye.", "ipa": "/ˌɪndɪˈstɪŋkt/"},
                        {"word": "maneuver", "pos": "n.", "meaning": "Động tác khéo léo", "example": "The gymnast performed a difficult maneuver.", "ipa": "/məˈnuːvər/"},
                        {"word": "performance", "pos": "n.", "meaning": "Màn trình diễn, hiệu suất thực hiện", "example": "Good vision improves athletic performance.", "ipa": "/pərˈfɔːrməns/"},
                        {"word": "peripheral", "pos": "adj.", "meaning": "Thuộc về vùng rìa, ngoại vi", "example": "Peripheral vision helps athletes see the whole field.", "ipa": "/pəˈrɪfərəl/"},
                        {"word": "range", "pos": "n.", "meaning": "Phạm vi, khu vực", "example": "Athletes need a wide range of vision.", "ipa": "/reɪndʒ/"},
                        {"word": "scan", "pos": "v.", "meaning": "Quan sát toàn bộ, nhìn lướt qua", "example": "Good players constantly scan the field.", "ipa": "/skæn/"},
                        {"word": "tolerate", "pos": "v.", "meaning": "Chấp nhận, chịu đựng", "example": "Elite athletes tolerate high levels of pressure.", "ipa": "/ˈtɒləreɪt/"},
                        {"word": "unconsciously", "pos": "adv.", "meaning": "Một cách vô thức, tự động", "example": "Athletes unconsciously track multiple objects.", "ipa": "/ʌnˈkɒnʃəsli/"},
                        {"word": "vision", "pos": "n.", "meaning": "Thị lực, khả năng nhìn", "example": "Good vision is essential for athletes.", "ipa": "/ˈvɪʒn/"}
                    ]
                },
                {
                    "name": "History of the Circus",
                    "words": [
                        {"word": "ancient", "pos": "adj.", "meaning": "Cổ đại, thuộc thời xa xưa", "example": "The ancient Romans enjoyed circus performances.", "ipa": "/ˈeɪnʃənt/"},
                        {"word": "band", "pos": "n.", "meaning": "Nhóm nhỏ người", "example": "A band of performers traveled with the circus.", "ipa": "/bænd/"},
                        {"word": "century", "pos": "n.", "meaning": "Thế kỷ, một trăm năm", "example": "The circus has evolved over many centuries.", "ipa": "/ˈsentʃəri/"},
                        {"word": "develop", "pos": "v.", "meaning": "Phát triển, thay đổi và lớn mạnh", "example": "The circus developed from ancient Roman games.", "ipa": "/dɪˈveləp/"},
                        {"word": "entertainment", "pos": "n.", "meaning": "Sự giải trí, màn biểu diễn", "example": "The circus was a popular form of entertainment.", "ipa": "/ˌentərˈteɪnmənt/"},
                        {"word": "exhibit", "pos": "n.", "meaning": "Triển lãm, vật được trưng bày", "example": "The circus exhibit attracted thousands of visitors.", "ipa": "/ɪɡˈzɪbɪt/"},
                        {"word": "exotic", "pos": "adj.", "meaning": "Kỳ lạ, đến từ nơi xa lạ", "example": "The circus featured exotic animals from Africa.", "ipa": "/ɪɡˈzɒtɪk/"},
                        {"word": "found", "pos": "v.", "meaning": "Sáng lập, thành lập", "example": "Barnum founded a famous circus in the 19th century.", "ipa": "/faʊnd/"},
                        {"word": "grandeur", "pos": "n.", "meaning": "Sự vĩ đại, huy hoàng", "example": "The circus was known for its grandeur.", "ipa": "/ˈɡrændjər/"},
                        {"word": "massive", "pos": "adj.", "meaning": "Rất lớn, khổng lồ", "example": "The Circus Maximus was a massive venue.", "ipa": "/ˈmæsɪv/"},
                        {"word": "permanently", "pos": "adv.", "meaning": "Vĩnh viễn, mãi mãi", "example": "The circus tent was not permanently located.", "ipa": "/ˈpɜːrmənəntli/"},
                        {"word": "popular", "pos": "adj.", "meaning": "Được nhiều người yêu thích", "example": "Acrobats were popular circus performers.", "ipa": "/ˈpɒpjələr/"},
                        {"word": "reduce", "pos": "v.", "meaning": "Giảm bớt, làm nhỏ lại", "example": "Modern circuses have reduced the use of animals.", "ipa": "/rɪˈdjuːs/"},
                        {"word": "remnant", "pos": "n.", "meaning": "Phần còn lại nhỏ", "example": "A remnant of the ancient circus still stands.", "ipa": "/ˈremnənt/"},
                        {"word": "renovation", "pos": "n.", "meaning": "Việc cải tạo, xây dựng lại", "example": "The circus tent underwent renovation.", "ipa": "/ˌrenəˈveɪʃn/"},
                        {"word": "spectator", "pos": "n.", "meaning": "Khán giả, người xem sự kiện", "example": "Thousands of spectators attended the circus.", "ipa": "/ˈspekteɪtər/"},
                        {"word": "survive", "pos": "v.", "meaning": "Tồn tại, tiếp tục sống", "example": "The circus tradition has survived for centuries.", "ipa": "/sərˈvaɪv/"},
                        {"word": "talent", "pos": "n.", "meaning": "Tài năng đặc biệt", "example": "Circus performers showed extraordinary talent.", "ipa": "/ˈtælənt/"},
                        {"word": "trainer", "pos": "n.", "meaning": "Huấn luyện viên dạy kỹ năng", "example": "Animal trainers worked closely with the performers.", "ipa": "/ˈtreɪnər/"},
                        {"word": "venue", "pos": "n.", "meaning": "Địa điểm tổ chức sự kiện", "example": "The venue for the circus was a large tent.", "ipa": "/ˈvenjuː/"}
                    ]
                },
                {
                    "name": "Uses of Leisure Time",
                    "words": [
                        {"word": "acknowledge", "pos": "v.", "meaning": "Thừa nhận, chấp nhận là thật", "example": "Researchers acknowledge the benefits of leisure.", "ipa": "/əkˈnɒlɪdʒ/"},
                        {"word": "authority", "pos": "n.", "meaning": "Người có quyền lực hoặc kiến thức chuyên môn", "example": "Health authorities recommend outdoor activities.", "ipa": "/ɔːˈθɒrəti/"},
                        {"word": "chunk", "pos": "n.", "meaning": "Một phần lớn", "example": "People spend a large chunk of time on screens.", "ipa": "/tʃʌŋk/"},
                        {"word": "crucial", "pos": "adj.", "meaning": "Cực kỳ quan trọng", "example": "Leisure time is crucial for mental health.", "ipa": "/ˈkruːʃl/"},
                        {"word": "deliberately", "pos": "adv.", "meaning": "Có chủ ý, có mục đích", "example": "People should deliberately plan leisure activities.", "ipa": "/dɪˈlɪbərətli/"},
                        {"word": "depression", "pos": "n.", "meaning": "Trầm cảm, nỗi buồn kéo dài", "example": "Lack of leisure time can lead to depression.", "ipa": "/dɪˈpreʃn/"},
                        {"word": "emotion", "pos": "n.", "meaning": "Cảm xúc, cảm giác mạnh mẽ", "example": "Leisure activities help regulate emotions.", "ipa": "/ɪˈmoʊʃn/"},
                        {"word": "engage", "pos": "v.", "meaning": "Tham gia, đắm mình vào điều gì", "example": "Children engage in outdoor activities.", "ipa": "/ɪnˈɡeɪdʒ/"},
                        {"word": "industrious", "pos": "adj.", "meaning": "Chăm chỉ, cần cù", "example": "Industrious people still need leisure time.", "ipa": "/ɪnˈdʌstriəs/"},
                        {"word": "intellectual", "pos": "adj.", "meaning": "Liên quan đến tư duy, trí tuệ", "example": "Reading is an intellectual leisure activity.", "ipa": "/ˌɪntəˈlektʃuəl/"},
                        {"word": "merely", "pos": "adv.", "meaning": "Chỉ, không hơn không kém", "example": "Leisure is not merely about relaxation.", "ipa": "/ˈmɪərli/"},
                        {"word": "obesity", "pos": "n.", "meaning": "Béo phì, tình trạng thừa cân nghiêm trọng", "example": "Sedentary leisure leads to obesity.", "ipa": "/oʊˈbiːsəti/"},
                        {"word": "obvious", "pos": "adj.", "meaning": "Rõ ràng, dễ thấy", "example": "The benefits of exercise are obvious.", "ipa": "/ˈɒbviəs/"},
                        {"word": "overwhelming", "pos": "adj.", "meaning": "Áp đảo, rất lớn", "example": "The evidence is overwhelming.", "ipa": "/ˌoʊvərˈwelmɪŋ/"},
                        {"word": "passive", "pos": "adj.", "meaning": "Thụ động, không chủ động", "example": "Watching TV is a passive activity.", "ipa": "/ˈpæsɪv/"},
                        {"word": "pastime", "pos": "n.", "meaning": "Hoạt động giải trí lúc rảnh rỗi", "example": "Reading is a popular pastime.", "ipa": "/ˈpæstaɪm/"},
                        {"word": "physical", "pos": "adj.", "meaning": "Liên quan đến thể chất, cơ thể", "example": "Physical activity improves mental health.", "ipa": "/ˈfɪzɪkl/"},
                        {"word": "rejuvenate", "pos": "v.", "meaning": "Tái tạo năng lượng, làm tươi trẻ lại", "example": "Time in nature rejuvenates the mind.", "ipa": "/rɪˈdʒuːvəneɪt/"},
                        {"word": "reluctant", "pos": "adj.", "meaning": "Miễn cưỡng, không muốn làm", "example": "Some people are reluctant to exercise.", "ipa": "/rɪˈlʌktənt/"},
                        {"word": "suffer", "pos": "v.", "meaning": "Trải qua điều khó khăn hay đau đớn", "example": "Overworked people suffer from burnout.", "ipa": "/ˈsʌfər/"}
                    ]
                }
            ]
        },
        {
            "id": 3,
            "name": "Transportation",
            "color": "#40916c",
            "topics": [
                {
                    "name": "First Headlamps",
                    "words": [
                        {"word": "cast", "pos": "v.", "meaning": "Chiếu sáng lên vật gì", "example": "Headlamps cast light on dark roads.", "ipa": "/kɑːst/"},
                        {"word": "disaster", "pos": "n.", "meaning": "Thảm họa, sự kiện khủng khiếp", "example": "Early lights caused many disasters.", "ipa": "/dɪˈzɑːstər/"},
                        {"word": "display", "pos": "v.", "meaning": "Trưng bày, trình diễn", "example": "Manufacturers display new lighting technology.", "ipa": "/dɪˈspleɪ/"},
                        {"word": "drawback", "pos": "n.", "meaning": "Nhược điểm, bất lợi", "example": "A major drawback of candles was the fire risk.", "ipa": "/ˈdrɔːbæk/"},
                        {"word": "efficient", "pos": "adj.", "meaning": "Hiệu quả, không lãng phí", "example": "Electric headlamps are more efficient.", "ipa": "/ɪˈfɪʃnt/"},
                        {"word": "equip", "pos": "v.", "meaning": "Trang bị, cung cấp thứ cần thiết", "example": "Vehicles were equipped with headlamps.", "ipa": "/ɪˈkwɪp/"},
                        {"word": "freight", "pos": "n.", "meaning": "Hàng hóa vận chuyển bằng tàu, xe tải", "example": "Freight trains transported goods at night.", "ipa": "/freɪt/"},
                        {"word": "generate", "pos": "v.", "meaning": "Tạo ra, sản xuất", "example": "Generators generate electricity for lights.", "ipa": "/ˈdʒenəreɪt/"},
                        {"word": "illuminator", "pos": "n.", "meaning": "Vật tạo ra ánh sáng", "example": "The illuminator provided enough light to see.", "ipa": "/ɪˈluːmɪneɪtər/"},
                        {"word": "innovation", "pos": "n.", "meaning": "Sáng kiến, ý tưởng hay sản phẩm mới", "example": "Electric lights were a major innovation.", "ipa": "/ˌɪnəˈveɪʃn/"},
                        {"word": "intense", "pos": "adj.", "meaning": "Rất mạnh, dữ dội", "example": "The intense light helped drivers see clearly.", "ipa": "/ɪnˈtens/"},
                        {"word": "knot", "pos": "n.", "meaning": "Chỗ cứng trên gỗ", "example": "The wooden lamp had a visible knot.", "ipa": "/nɒt/"},
                        {"word": "locomotive", "pos": "n.", "meaning": "Đầu máy xe lửa", "example": "Locomotives needed powerful headlamps.", "ipa": "/ˈloʊkəmoʊtɪv/"},
                        {"word": "mode", "pos": "n.", "meaning": "Phương thức, phương pháp", "example": "Different modes of transport use different lights.", "ipa": "/moʊd/"},
                        {"word": "portable", "pos": "adj.", "meaning": "Dễ mang vác, có thể di chuyển", "example": "Portable lanterns were used in early vehicles.", "ipa": "/ˈpɔːrtəbl/"},
                        {"word": "reflector", "pos": "n.", "meaning": "Vật phản chiếu ánh sáng", "example": "Reflectors made the lights more visible.", "ipa": "/rɪˈflektər/"},
                        {"word": "rugged", "pos": "adj.", "meaning": "Chắc chắn, chịu được điều kiện khắc nghiệt", "example": "Early headlamps needed to be rugged.", "ipa": "/ˈrʌɡɪd/"},
                        {"word": "stringent", "pos": "adj.", "meaning": "Nghiêm ngặt, chặt chẽ", "example": "Stringent safety rules govern vehicle lights.", "ipa": "/ˈstrɪndʒənt/"},
                        {"word": "tricky", "pos": "adj.", "meaning": "Khó khăn, phức tạp", "example": "Making reliable portable lights was tricky.", "ipa": "/ˈtrɪki/"},
                        {"word": "vulnerable", "pos": "adj.", "meaning": "Dễ bị tổn thương, không được bảo vệ", "example": "Flame lights are vulnerable to wind.", "ipa": "/ˈvʌlnərəbl/"}
                    ]
                },
                {
                    "name": "Electric Cars Around the Globe",
                    "words": [
                        {"word": "accelerate", "pos": "v.", "meaning": "Tăng tốc độ", "example": "Electric cars can accelerate quickly.", "ipa": "/əkˈseləreɪt/"},
                        {"word": "appeal", "pos": "v.", "meaning": "Thu hút, có sức hấp dẫn", "example": "Electric cars appeal to eco-conscious buyers.", "ipa": "/əˈpiːl/"},
                        {"word": "charge", "pos": "n.", "meaning": "Lượng điện mà pin có thể lưu trữ", "example": "A full charge lasts 300 miles.", "ipa": "/tʃɑːrdʒ/"},
                        {"word": "classify", "pos": "v.", "meaning": "Phân loại theo nhóm", "example": "Cars are classified by fuel type.", "ipa": "/ˈklæsɪfaɪ/"},
                        {"word": "commuter", "pos": "n.", "meaning": "Người đi lại thường xuyên giữa nhà và nơi làm việc", "example": "Commuters benefit from electric cars.", "ipa": "/kəˈmjuːtər/"},
                        {"word": "consume", "pos": "v.", "meaning": "Tiêu thụ, sử dụng", "example": "Electric cars consume less energy.", "ipa": "/kənˈsjuːm/"},
                        {"word": "embrace", "pos": "v.", "meaning": "Chấp nhận một cách nhiệt tình", "example": "Many countries have embraced electric cars.", "ipa": "/ɪmˈbreɪs/"},
                        {"word": "flair", "pos": "n.", "meaning": "Phong cách thanh lịch, sự duyên dáng", "example": "The car's design had European flair.", "ipa": "/fleər/"},
                        {"word": "fume", "pos": "n.", "meaning": "Khí thải độc hại", "example": "Electric cars produce no fumes.", "ipa": "/fjuːm/"},
                        {"word": "hamper", "pos": "v.", "meaning": "Cản trở, gây khó khăn", "example": "Limited charging stations hamper adoption.", "ipa": "/ˈhæmpər/"},
                        {"word": "incentive", "pos": "n.", "meaning": "Động lực, phần thưởng khuyến khích", "example": "Tax incentives encourage electric car purchases.", "ipa": "/ɪnˈsentɪv/"},
                        {"word": "markedly", "pos": "adv.", "meaning": "Một cách đáng chú ý, rõ rệt", "example": "Sales have markedly increased.", "ipa": "/ˈmɑːrkɪdli/"},
                        {"word": "monetary", "pos": "adj.", "meaning": "Liên quan đến tiền tệ", "example": "Monetary incentives help boost sales.", "ipa": "/ˈmɒnɪtəri/"},
                        {"word": "plodding", "pos": "adj.", "meaning": "Chậm chạp, lề mề", "example": "Early electric cars had a plodding pace.", "ipa": "/ˈplɒdɪŋ/"},
                        {"word": "rural", "pos": "adj.", "meaning": "Liên quan đến vùng nông thôn", "example": "Rural areas lack charging infrastructure.", "ipa": "/ˈrʊərəl/"},
                        {"word": "span", "pos": "v.", "meaning": "Trải dài qua, bắc qua", "example": "Electric car adoption spans many countries.", "ipa": "/spæn/"},
                        {"word": "sprawl", "pos": "n.", "meaning": "Khu vực phát triển lan rộng", "example": "Urban sprawl makes commuting longer.", "ipa": "/sprɔːl/"},
                        {"word": "standard", "pos": "n.", "meaning": "Tiêu chuẩn, điều thông thường phổ biến", "example": "Gasoline became the standard fuel.", "ipa": "/ˈstændərd/"},
                        {"word": "suburban", "pos": "adj.", "meaning": "Thuộc vùng ngoại ô, ven thành phố", "example": "Suburban commuters prefer electric cars.", "ipa": "/səˈbɜːrbən/"},
                        {"word": "urban", "pos": "adj.", "meaning": "Thuộc về thành phố, đô thị", "example": "Urban areas have more charging stations.", "ipa": "/ˈɜːrbən/"}
                    ]
                }
            ]
        },
        {
            "id": 4,
            "name": "Culture",
            "color": "#52b788",
            "topics": [
                {
                    "name": "Origins of Writing",
                    "words": [
                        {"word": "adopt", "pos": "v.", "meaning": "Áp dụng, bắt đầu sử dụng cái gì mới", "example": "Ancient civilizations adopted writing systems.", "ipa": "/əˈdɒpt/"},
                        {"word": "agricultural", "pos": "adj.", "meaning": "Liên quan đến nông nghiệp", "example": "Agricultural records required writing.", "ipa": "/ˌæɡrɪˈkʌltʃərəl/"},
                        {"word": "attribute", "pos": "v.", "meaning": "Quy công cho, coi là nguồn gốc của", "example": "Ancients attributed writing to the gods.", "ipa": "/əˈtrɪbjuːt/"},
                        {"word": "carve", "pos": "v.", "meaning": "Khắc, chạm trổ vật cứng", "example": "Scribes carved symbols into stone tablets.", "ipa": "/kɑːrv/"},
                        {"word": "civilization", "pos": "n.", "meaning": "Nền văn minh, xã hội loài người", "example": "Writing marked the rise of civilization.", "ipa": "/ˌsɪvəlaɪˈzeɪʃn/"},
                        {"word": "creator", "pos": "n.", "meaning": "Người tạo ra điều gì lần đầu tiên", "example": "Ancient peoples believed gods were writing's creator.", "ipa": "/kriˈeɪtər/"},
                        {"word": "deed", "pos": "n.", "meaning": "Hành động, việc làm tốt hoặc xấu", "example": "Deeds of kings were recorded in writing.", "ipa": "/diːd/"},
                        {"word": "encompass", "pos": "v.", "meaning": "Bao gồm, bao hàm", "example": "Writing encompasses many different systems.", "ipa": "/ɪnˈkʌmpəs/"},
                        {"word": "excavation", "pos": "n.", "meaning": "Khu khai quật khảo cổ", "example": "Excavations revealed ancient written tablets.", "ipa": "/ˌekskəˈveɪʃn/"},
                        {"word": "function", "pos": "v.", "meaning": "Hoạt động tốt, thực hiện chức năng", "example": "Early writing functioned as a record-keeping tool.", "ipa": "/ˈfʌŋkʃn/"},
                        {"word": "inscribe", "pos": "v.", "meaning": "Khắc chữ lên bề mặt", "example": "Priests inscribed prayers on temple walls.", "ipa": "/ɪnˈskraɪb/"},
                        {"word": "literacy", "pos": "n.", "meaning": "Khả năng đọc và viết", "example": "Literacy spread with the printing press.", "ipa": "/ˈlɪtərəsi/"},
                        {"word": "mythology", "pos": "n.", "meaning": "Thần thoại, hệ thống truyền thuyết truyền thống", "example": "Writing origins appear in Greek mythology.", "ipa": "/mɪˈθɒlədʒi/"},
                        {"word": "property", "pos": "n.", "meaning": "Tài sản, vật sở hữu", "example": "Writing helped track property ownership.", "ipa": "/ˈprɒpəti/"},
                        {"word": "scholar", "pos": "n.", "meaning": "Học giả, người có kiến thức sâu rộng", "example": "Scholars study the origins of writing.", "ipa": "/ˈskɒlər/"},
                        {"word": "settle", "pos": "v.", "meaning": "Định cư, thiết lập nơi ở lâu dài", "example": "People settled in river valleys.", "ipa": "/ˈsetl/"},
                        {"word": "specialized", "pos": "adj.", "meaning": "Chuyên biệt, liên quan đến lĩnh vực cụ thể", "example": "Writing required specialized knowledge.", "ipa": "/ˈspeʃəlaɪzd/"},
                        {"word": "structure", "pos": "n.", "meaning": "Công trình xây dựng, cấu trúc", "example": "Ancient structures contained written inscriptions.", "ipa": "/ˈstrʌktʃər/"},
                        {"word": "tablet", "pos": "n.", "meaning": "Tấm phẳng mỏng dùng để viết", "example": "Clay tablets preserved ancient writing.", "ipa": "/ˈtæblɪt/"},
                        {"word": "token", "pos": "n.", "meaning": "Vật dùng để đại diện cho thứ khác", "example": "Clay tokens preceded written symbols.", "ipa": "/ˈtoʊkən/"}
                    ]
                },
                {
                    "name": "Hula Dancing in Hawaiian Culture",
                    "words": [
                        {"word": "accompany", "pos": "v.", "meaning": "Đi cùng, xảy ra đồng thời", "example": "Music accompanies traditional hula dance.", "ipa": "/əˈkʌmpəni/"},
                        {"word": "altar", "pos": "n.", "meaning": "Bàn thờ dùng trong các buổi lễ tôn giáo", "example": "Offerings were placed on the altar.", "ipa": "/ˈɔːltər/"},
                        {"word": "benefit", "pos": "n.", "meaning": "Lợi ích, điều có lợi", "example": "Hula dancing has health benefits.", "ipa": "/ˈbenɪfɪt/"},
                        {"word": "celebration", "pos": "n.", "meaning": "Lễ kỷ niệm, sự kiện để đánh dấu ngày đặc biệt", "example": "Hula is performed during celebrations.", "ipa": "/ˌselɪˈbreɪʃn/"},
                        {"word": "discourage", "pos": "v.", "meaning": "Ngăn cản, cố gắng ngăn chặn điều gì", "example": "Missionaries discouraged traditional dancing.", "ipa": "/dɪˈskʌrɪdʒ/"},
                        {"word": "elaborate", "pos": "adj.", "meaning": "Công phu, tỉ mỉ với nhiều chi tiết", "example": "Hula costumes are elaborate and beautiful.", "ipa": "/ɪˈlæbərət/"},
                        {"word": "energetic", "pos": "adj.", "meaning": "Đầy năng lượng, sôi động", "example": "Modern hula is energetic and expressive.", "ipa": "/ˌenərˈdʒetɪk/"},
                        {"word": "evidence", "pos": "n.", "meaning": "Bằng chứng, dấu hiệu chứng minh", "example": "Evidence shows hula dates back centuries.", "ipa": "/ˈevɪdəns/"},
                        {"word": "evoke", "pos": "v.", "meaning": "Gợi lên, khơi dậy ký ức hoặc cảm xúc", "example": "Hula movements evoke nature.", "ipa": "/ɪˈvoʊk/"},
                        {"word": "floral", "pos": "adj.", "meaning": "Liên quan đến hoa, có hình hoa", "example": "Dancers wear floral garlands.", "ipa": "/ˈflɔːrəl/"},
                        {"word": "garland", "pos": "n.", "meaning": "Vòng hoa trang trí", "example": "Lei is a traditional Hawaiian garland.", "ipa": "/ˈɡɑːrlənd/"},
                        {"word": "graceful", "pos": "adj.", "meaning": "Duyên dáng, đẹp về chuyển động", "example": "Hula dancers are graceful performers.", "ipa": "/ˈɡreɪsfl/"},
                        {"word": "image", "pos": "n.", "meaning": "Hình ảnh, bức tranh trong tâm trí", "example": "Hula creates vivid images of Hawaii.", "ipa": "/ˈɪmɪdʒ/"},
                        {"word": "influence", "pos": "n.", "meaning": "Tầm ảnh hưởng, quyền lực tác động", "example": "Western culture had great influence on hula.", "ipa": "/ˈɪnfluəns/"},
                        {"word": "reign", "pos": "n.", "meaning": "Triều đại, thời gian một vua hay hoàng hậu cầm quyền", "example": "Hula was revived during King Kalakaua's reign.", "ipa": "/reɪn/"},
                        {"word": "revive", "pos": "v.", "meaning": "Hồi sinh, đưa trở lại cuộc sống", "example": "King Kalakaua worked to revive hula.", "ipa": "/rɪˈvaɪv/"},
                        {"word": "ritual", "pos": "n.", "meaning": "Nghi lễ, phong tục truyền thống", "example": "Hula began as a sacred ritual.", "ipa": "/ˈrɪtʃuəl/"},
                        {"word": "stereotype", "pos": "n.", "meaning": "Định kiến, quan niệm cố định sai lầm", "example": "Modern hula challenges old stereotypes.", "ipa": "/ˈsteriətaɪp/"},
                        {"word": "sway", "pos": "v.", "meaning": "Lắc lư, đung đưa", "example": "Hula dancers sway their hips gracefully.", "ipa": "/sweɪ/"},
                        {"word": "tradition", "pos": "n.", "meaning": "Truyền thống, phong tục của một nhóm người", "example": "Hula is an ancient Hawaiian tradition.", "ipa": "/trəˈdɪʃn/"}
                    ]
                },
                {
                    "name": "The Art of Mime",
                    "words": [
                        {"word": "abstract", "pos": "adj.", "meaning": "Trừu tượng, liên quan đến ý tưởng hơn là vật thể cụ thể", "example": "Mime conveys abstract emotions through gesture.", "ipa": "/ˈæbstrækt/"},
                        {"word": "atmosphere", "pos": "n.", "meaning": "Bầu không khí, cảm giác của một nơi", "example": "A good mime creates a believable atmosphere.", "ipa": "/ˈætməsfɪər/"},
                        {"word": "conflict", "pos": "n.", "meaning": "Xung đột, sự đối lập", "example": "Mime often portrays inner conflict.", "ipa": "/ˈkɒnflɪkt/"},
                        {"word": "considerably", "pos": "adv.", "meaning": "Đáng kể, nhiều", "example": "Mime has changed considerably over time.", "ipa": "/kənˈsɪdərəbli/"},
                        {"word": "culminate", "pos": "v.", "meaning": "Đạt đến đỉnh điểm, kết thúc với", "example": "The performance culminated in a standing ovation.", "ipa": "/ˈkʌlmɪneɪt/"},
                        {"word": "effectively", "pos": "adv.", "meaning": "Một cách hiệu quả, thành công", "example": "Mime communicates effectively without words.", "ipa": "/ɪˈfektɪvli/"},
                        {"word": "emerge", "pos": "v.", "meaning": "Xuất hiện, phát triển", "example": "Mime emerged from ancient Greek theater.", "ipa": "/ɪˈmɜːrdʒ/"},
                        {"word": "exaggerated", "pos": "adj.", "meaning": "Phóng đại, được thể hiện to hơn thực tế", "example": "Mime uses exaggerated gestures.", "ipa": "/ɪɡˈzædʒəreɪtɪd/"},
                        {"word": "frailty", "pos": "n.", "meaning": "Sự yếu đuối, thiếu sức mạnh", "example": "Mime often portrays human frailty.", "ipa": "/ˈfreɪlti/"},
                        {"word": "gesture", "pos": "n.", "meaning": "Cử chỉ, động tác để biểu đạt cảm xúc", "example": "Every gesture in mime has meaning.", "ipa": "/ˈdʒestʃər/"},
                        {"word": "humorous", "pos": "adj.", "meaning": "Hài hước, giải trí", "example": "Chaplin's mime was often humorous.", "ipa": "/ˈhjuːmərəs/"},
                        {"word": "illusion", "pos": "n.", "meaning": "Ảo giác, ấn tượng giả tạo về thực tế", "example": "Mime creates the illusion of invisible walls.", "ipa": "/ɪˈluːʒn/"},
                        {"word": "literal", "pos": "adj.", "meaning": "Theo nghĩa đen, chính xác", "example": "Mime takes a literal approach to storytelling.", "ipa": "/ˈlɪtərəl/"},
                        {"word": "merge", "pos": "v.", "meaning": "Hòa nhập, kết hợp", "example": "Drama and dance merge in mime.", "ipa": "/mɜːrdʒ/"},
                        {"word": "portray", "pos": "v.", "meaning": "Thể hiện, diễn tả", "example": "Mimes portray everyday situations.", "ipa": "/pɔːrˈtreɪ/"},
                        {"word": "prominent", "pos": "adj.", "meaning": "Nổi bật, quan trọng", "example": "Marcel Marceau was a prominent mime artist.", "ipa": "/ˈprɒmɪnənt/"},
                        {"word": "prop", "pos": "n.", "meaning": "Đạo cụ, vật dụng của diễn viên", "example": "Mime uses no props — only the body.", "ipa": "/prɒp/"},
                        {"word": "reminiscent", "pos": "adj.", "meaning": "Gợi nhớ, nhắc nhở về điều gì", "example": "Modern mime is reminiscent of Chaplin's style.", "ipa": "/ˌremɪˈnɪsnt/"},
                        {"word": "renowned", "pos": "adj.", "meaning": "Nổi tiếng, được nhiều người biết đến", "example": "Marcel Marceau was renowned worldwide.", "ipa": "/rɪˈnaʊnd/"},
                        {"word": "sharpen", "pos": "v.", "meaning": "Mài sắc, cải thiện, hoàn thiện", "example": "Practice sharpens a mime's skills.", "ipa": "/ˈʃɑːrpən/"}
                    ]
                }
            ]
        },
        {
            "id": 5,
            "name": "Health",
            "color": "#74c69d",
            "topics": [
                {
                    "name": "Nurse Migration",
                    "words": [
                        {"word": "abroad", "pos": "adv.", "meaning": "Ở nước ngoài, tại đất nước khác", "example": "Many nurses work abroad for better pay.", "ipa": "/əˈbrɔːd/"},
                        {"word": "administer", "pos": "v.", "meaning": "Cung cấp thuốc hoặc điều trị y tế", "example": "Nurses administer medication to patients.", "ipa": "/ədˈmɪnɪstər/"},
                        {"word": "bulk", "pos": "n.", "meaning": "Phần lớn nhất, số lượng tổng cộng", "example": "The bulk of nurses come from the Philippines.", "ipa": "/bʌlk/"},
                        {"word": "complex", "pos": "adj.", "meaning": "Phức tạp, không đơn giản", "example": "The nursing shortage is a complex problem.", "ipa": "/ˈkɒmpleks/"},
                        {"word": "cripple", "pos": "v.", "meaning": "Gây tổn hại nghiêm trọng, làm suy yếu", "example": "A shortage could cripple the health system.", "ipa": "/ˈkrɪpl/"},
                        {"word": "decade", "pos": "n.", "meaning": "Thập kỷ, khoảng mười năm", "example": "The shortage has grown over a decade.", "ipa": "/ˈdekeɪd/"},
                        {"word": "decline", "pos": "v.", "meaning": "Giảm dần, trở nên ít hơn", "example": "The number of nurses has declined.", "ipa": "/dɪˈklaɪn/"},
                        {"word": "epidemic", "pos": "n.", "meaning": "Dịch bệnh, sự lây lan nhanh của bệnh tật", "example": "The nursing shortage is reaching epidemic levels.", "ipa": "/ˌepɪˈdemɪk/"},
                        {"word": "estimate", "pos": "v.", "meaning": "Ước tính dựa trên thông tin có sẵn", "example": "Experts estimate a shortage of one million nurses.", "ipa": "/ˈestɪmeɪt/"},
                        {"word": "lure", "pos": "v.", "meaning": "Thu hút, dụ dỗ", "example": "Higher salaries lure nurses abroad.", "ipa": "/lʊər/"},
                        {"word": "primary", "pos": "adj.", "meaning": "Chính, quan trọng nhất", "example": "The primary reason for migration is better pay.", "ipa": "/ˈpraɪməri/"},
                        {"word": "qualified", "pos": "adj.", "meaning": "Có năng lực, đủ tiêu chuẩn làm việc", "example": "Qualified nurses are in high demand.", "ipa": "/ˈkwɒlɪfaɪd/"},
                        {"word": "rampant", "pos": "adj.", "meaning": "Lan rộng không kiểm soát được", "example": "Rampant migration is causing shortages.", "ipa": "/ˈræmpənt/"},
                        {"word": "retain", "pos": "v.", "meaning": "Giữ lại, không để mất", "example": "Countries struggle to retain qualified nurses.", "ipa": "/rɪˈteɪn/"},
                        {"word": "rudimentary", "pos": "adj.", "meaning": "Cơ bản, chưa được phát triển đầy đủ", "example": "Some areas only have rudimentary healthcare.", "ipa": "/ˌruːdɪˈmentəri/"},
                        {"word": "shortage", "pos": "n.", "meaning": "Sự thiếu hụt", "example": "There is a global nursing shortage.", "ipa": "/ˈʃɔːrtɪdʒ/"},
                        {"word": "standpoint", "pos": "n.", "meaning": "Quan điểm, góc nhìn", "example": "From an economic standpoint, migration helps.", "ipa": "/ˈstændpɔɪnt/"},
                        {"word": "stem", "pos": "v.", "meaning": "Bắt nguồn từ, xuất phát từ", "example": "The shortage stems from low salaries.", "ipa": "/stem/"},
                        {"word": "supply", "pos": "n.", "meaning": "Nguồn cung, tổng lượng có sẵn", "example": "The supply of nurses is insufficient.", "ipa": "/səˈplaɪ/"},
                        {"word": "vacancy", "pos": "n.", "meaning": "Vị trí trống, công việc cần được lấp đầy", "example": "Hospitals have many vacancies.", "ipa": "/ˈveɪkənsi/"}
                    ]
                },
                {
                    "name": "Aerobic Exercise and Brain Health",
                    "words": [
                        {"word": "aerobic", "pos": "adj.", "meaning": "Liên quan đến tập thể dục cường độ cao", "example": "Aerobic exercise improves cardiovascular health.", "ipa": "/eəˈroʊbɪk/"},
                        {"word": "capacity", "pos": "n.", "meaning": "Năng lực, tổng lượng sẵn có", "example": "Exercise increases brain capacity.", "ipa": "/kəˈpæsəti/"},
                        {"word": "cognition", "pos": "n.", "meaning": "Nhận thức, việc sử dụng các quá trình tư duy", "example": "Exercise improves cognition in older adults.", "ipa": "/kɒɡˈnɪʃn/"},
                        {"word": "concentration", "pos": "n.", "meaning": "Lượng lớn tập trung ở một nơi", "example": "Exercise improves concentration and focus.", "ipa": "/ˌkɒnsənˈtreɪʃn/"},
                        {"word": "counteract", "pos": "v.", "meaning": "Chống lại, làm vô hiệu hóa", "example": "Exercise counteracts the effects of aging.", "ipa": "/ˌkaʊntərˈækt/"},
                        {"word": "dementia", "pos": "n.", "meaning": "Chứng mất trí nhớ, suy giảm chức năng não", "example": "Exercise may help prevent dementia.", "ipa": "/dɪˈmenʃə/"},
                        {"word": "deterioration", "pos": "n.", "meaning": "Sự suy giảm, trở nên tệ hơn", "example": "Exercise slows brain deterioration.", "ipa": "/dɪˌtɪəriəˈreɪʃn/"},
                        {"word": "diagnose", "pos": "v.", "meaning": "Chẩn đoán bệnh tật", "example": "Doctors diagnose dementia through brain scans.", "ipa": "/ˈdaɪəɡnoʊz/"},
                        {"word": "disorder", "pos": "n.", "meaning": "Bệnh lý, tình trạng rối loạn", "example": "Exercise helps treat mood disorders.", "ipa": "/dɪˈsɔːrdər/"},
                        {"word": "gravity", "pos": "n.", "meaning": "Mức độ nghiêm trọng", "example": "The gravity of the problem is underestimated.", "ipa": "/ˈɡrævəti/"},
                        {"word": "impaired", "pos": "adj.", "meaning": "Bị suy giảm, bị tổn hại", "example": "Memory can become impaired with age.", "ipa": "/ɪmˈpeərd/"},
                        {"word": "indicate", "pos": "v.", "meaning": "Chỉ ra, cho thấy", "example": "Research indicates exercise helps the brain.", "ipa": "/ˈɪndɪkeɪt/"},
                        {"word": "link", "pos": "n.", "meaning": "Mối liên hệ, kết nối", "example": "There is a clear link between exercise and health.", "ipa": "/lɪŋk/"},
                        {"word": "mood", "pos": "n.", "meaning": "Tâm trạng, trạng thái cảm xúc", "example": "Exercise can improve mood significantly.", "ipa": "/muːd/"},
                        {"word": "previously", "pos": "adv.", "meaning": "Trước đây, trước đó", "example": "Previously unknown benefits are being discovered.", "ipa": "/ˈpriːviəsli/"},
                        {"word": "regulate", "pos": "v.", "meaning": "Điều chỉnh, kiểm soát", "example": "Exercise regulates stress hormones.", "ipa": "/ˈreɡjəleɪt/"},
                        {"word": "rodent", "pos": "n.", "meaning": "Loài gặm nhấm như chuột", "example": "Rodents were used in early exercise studies.", "ipa": "/ˈroʊdnt/"},
                        {"word": "spatial", "pos": "adj.", "meaning": "Liên quan đến không gian", "example": "Exercise improves spatial reasoning.", "ipa": "/ˈspeɪʃl/"},
                        {"word": "stave off", "pos": "v.", "meaning": "Ngăn ngừa, trì hoãn", "example": "Exercise can stave off cognitive decline.", "ipa": "/steɪv ɒf/"},
                        {"word": "stimulate", "pos": "v.", "meaning": "Kích thích, gây ra phản ứng", "example": "Exercise stimulates brain cell growth.", "ipa": "/ˈstɪmjəleɪt/"}
                    ]
                },
                {
                    "name": "How Drugs Are Studied",
                    "words": [
                        {"word": "absorb", "pos": "v.", "meaning": "Hấp thụ, tiếp nhận vào cơ thể", "example": "The body absorbs medication at different rates.", "ipa": "/əbˈsɔːrb/"},
                        {"word": "alleviate", "pos": "v.", "meaning": "Làm giảm nhẹ, xoa dịu", "example": "New drugs alleviate pain effectively.", "ipa": "/əˈliːvieɪt/"},
                        {"word": "ascertain", "pos": "v.", "meaning": "Xác định, tìm ra chắc chắn", "example": "Scientists ascertain drug safety through trials.", "ipa": "/ˌæsərˈteɪn/"},
                        {"word": "chronic", "pos": "adj.", "meaning": "Mãn tính, kéo dài", "example": "Chronic pain requires long-term treatment.", "ipa": "/ˈkrɒnɪk/"},
                        {"word": "combat", "pos": "v.", "meaning": "Chiến đấu chống lại", "example": "New vaccines combat infectious diseases.", "ipa": "/ˈkɒmbæt/"},
                        {"word": "culture", "pos": "n.", "meaning": "Nuôi cấy sinh vật trong phòng thí nghiệm", "example": "Drug testing begins in laboratory cultures.", "ipa": "/ˈkʌltʃər/"},
                        {"word": "deem", "pos": "v.", "meaning": "Coi là, đánh giá là", "example": "Scientists deem a drug safe after testing.", "ipa": "/diːm/"},
                        {"word": "desirable", "pos": "adj.", "meaning": "Đáng mong muốn, có giá trị", "example": "Researchers look for desirable drug effects.", "ipa": "/dɪˈzaɪərəbl/"},
                        {"word": "enhance", "pos": "v.", "meaning": "Cải thiện, nâng cao", "example": "Some drugs enhance cognitive performance.", "ipa": "/ɪnˈhɑːns/"},
                        {"word": "fraction", "pos": "n.", "meaning": "Phần nhỏ", "example": "Only a fraction of drugs reach the market.", "ipa": "/ˈfrækʃn/"},
                        {"word": "interval", "pos": "n.", "meaning": "Khoảng thời gian giữa hai thời điểm", "example": "Drugs are administered at regular intervals.", "ipa": "/ˈɪntərvl/"},
                        {"word": "investigation", "pos": "n.", "meaning": "Cuộc điều tra, nghiên cứu", "example": "Drug investigation takes many years.", "ipa": "/ɪnˌvestɪˈɡeɪʃn/"},
                        {"word": "manufacture", "pos": "v.", "meaning": "Sản xuất, chế tạo", "example": "Factories manufacture approved drugs.", "ipa": "/ˌmænjəˈfæktʃər/"},
                        {"word": "monitor", "pos": "v.", "meaning": "Theo dõi, quan sát", "example": "Doctors monitor patients during drug trials.", "ipa": "/ˈmɒnɪtər/"},
                        {"word": "outcome", "pos": "n.", "meaning": "Kết quả, hậu quả", "example": "Positive outcomes lead to drug approval.", "ipa": "/ˈaʊtkʌm/"},
                        {"word": "recur", "pos": "v.", "meaning": "Tái phát, xảy ra lại", "example": "Some diseases recur after treatment stops.", "ipa": "/rɪˈkɜːr/"},
                        {"word": "substance", "pos": "n.", "meaning": "Chất, vật liệu", "example": "New substances are tested for medicinal use.", "ipa": "/ˈsʌbstəns/"},
                        {"word": "target", "pos": "v.", "meaning": "Nhắm vào, tập trung vào", "example": "Scientists target specific disease pathways.", "ipa": "/ˈtɑːrɡɪt/"},
                        {"word": "theoretical", "pos": "adj.", "meaning": "Lý thuyết, dựa trên lý thuyết", "example": "Drug development starts at the theoretical stage.", "ipa": "/ˌθɪəˈretɪkl/"},
                        {"word": "toxic", "pos": "adj.", "meaning": "Độc hại, gây nguy hiểm", "example": "Drugs are tested for toxic side effects.", "ipa": "/ˈtɒksɪk/"}
                    ]
                }
            ]
        },
        {
            "id": 6,
            "name": "Tourism",
            "color": "#95d5b2",
            "topics": [
                {
                    "name": "Hiking the Inca Trail",
                    "words": [
                        {"word": "accessible", "pos": "adj.", "meaning": "Có thể tiếp cận, dễ đến", "example": "The Inca Trail is accessible to experienced hikers.", "ipa": "/əkˈsesəbl/"},
                        {"word": "adventurous", "pos": "adj.", "meaning": "Dũng cảm, thích thử nghiệm mới", "example": "The hike attracts adventurous travelers.", "ipa": "/ədˈventʃərəs/"},
                        {"word": "archaeologist", "pos": "n.", "meaning": "Nhà khảo cổ học nghiên cứu nền văn hóa cổ đại", "example": "Archaeologists have studied the Inca ruins.", "ipa": "/ˌɑːrkiˈɒlədʒɪst/"},
                        {"word": "ceremonial", "pos": "adj.", "meaning": "Liên quan đến nghi lễ truyền thống trang trọng", "example": "Machu Picchu had ceremonial significance.", "ipa": "/ˌserɪˈmoʊniəl/"},
                        {"word": "construct", "pos": "v.", "meaning": "Xây dựng, tạo dựng", "example": "The Incas constructed an amazing trail system.", "ipa": "/kənˈstrʌkt/"},
                        {"word": "draw", "pos": "v.", "meaning": "Thu hút, kéo đến", "example": "The trail draws thousands of tourists yearly.", "ipa": "/drɔː/"},
                        {"word": "imagination", "pos": "n.", "meaning": "Trí tưởng tượng, khả năng tư duy sáng tạo", "example": "The ruins capture the visitor's imagination.", "ipa": "/ɪˌmædʒɪˈneɪʃn/"},
                        {"word": "institute", "pos": "v.", "meaning": "Thiết lập, đưa vào thực hiện", "example": "The government instituted limits on hikers.", "ipa": "/ˈɪnstɪtjuːt/"},
                        {"word": "luxury", "pos": "n.", "meaning": "Xa xỉ phẩm, điều đắt tiền không cần thiết", "example": "Some tours offer luxury camping.", "ipa": "/ˈlʌkʃəri/"},
                        {"word": "marvel", "pos": "n.", "meaning": "Điều kỳ diệu, thứ tuyệt vời", "example": "Machu Picchu is a marvel of engineering.", "ipa": "/ˈmɑːrvl/"},
                        {"word": "mystery", "pos": "n.", "meaning": "Bí ẩn, điều kỳ lạ khó giải thích", "example": "The Inca Trail is shrouded in mystery.", "ipa": "/ˈmɪstəri/"},
                        {"word": "native", "pos": "adj.", "meaning": "Bản địa, có nguồn gốc từ nơi đó", "example": "Native guides help tourists on the trail.", "ipa": "/ˈneɪtɪv/"},
                        {"word": "network", "pos": "n.", "meaning": "Mạng lưới các bộ phận hoạt động cùng nhau", "example": "The Incas built an extensive trail network.", "ipa": "/ˈnetwɜːrk/"},
                        {"word": "pertain", "pos": "v.", "meaning": "Liên quan đến, có mối quan hệ với", "example": "Rules pertain to the number of hikers allowed.", "ipa": "/pərˈteɪn/"},
                        {"word": "precisely", "pos": "adv.", "meaning": "Chính xác, đúng như vậy", "example": "The trail is precisely 26 miles long.", "ipa": "/prɪˈsaɪsli/"},
                        {"word": "preserve", "pos": "v.", "meaning": "Bảo tồn, gìn giữ", "example": "Peru works hard to preserve the trail.", "ipa": "/prɪˈzɜːrv/"},
                        {"word": "restriction", "pos": "n.", "meaning": "Giới hạn chính thức, hạn chế", "example": "Visitor restrictions protect the ruins.", "ipa": "/rɪˈstrɪkʃn/"},
                        {"word": "site", "pos": "n.", "meaning": "Địa điểm, khu vực", "example": "Machu Picchu is a UNESCO World Heritage site.", "ipa": "/saɪt/"},
                        {"word": "spectacular", "pos": "adj.", "meaning": "Ngoạn mục, tuyệt vời khi nhìn thấy", "example": "The views from the trail are spectacular.", "ipa": "/spekˈtækjələr/"},
                        {"word": "upside", "pos": "n.", "meaning": "Mặt tích cực, lợi thế", "example": "The upside of the hike is the stunning views.", "ipa": "/ˈʌpsaɪd/"}
                    ]
                },
                {
                    "name": "What Is Ecotourism?",
                    "words": [
                        {"word": "accommodations", "pos": "n.", "meaning": "Chỗ ở như khách sạn", "example": "Eco-lodges offer sustainable accommodations.", "ipa": "/əˌkɒməˈdeɪʃnz/"},
                        {"word": "avoid", "pos": "v.", "meaning": "Tránh, không để xảy ra", "example": "Ecotourists avoid polluting natural areas.", "ipa": "/əˈvɔɪd/"},
                        {"word": "barrier", "pos": "n.", "meaning": "Rào cản, thứ ngăn cản hoặc phân tách", "example": "Cost is a barrier to ecotourism.", "ipa": "/ˈbæriər/"},
                        {"word": "category", "pos": "n.", "meaning": "Nhóm, loại có điểm chung", "example": "Ecotourism falls into a unique category.", "ipa": "/ˈkætəɡɔːri/"},
                        {"word": "concept", "pos": "n.", "meaning": "Khái niệm, ý tưởng", "example": "The concept of ecotourism is growing.", "ipa": "/ˈkɒnsept/"},
                        {"word": "culprit", "pos": "n.", "meaning": "Kẻ có lỗi, nguyên nhân của vấn đề", "example": "Tourism is a culprit of environmental damage.", "ipa": "/ˈkʌlprɪt/"},
                        {"word": "delicate", "pos": "adj.", "meaning": "Mong manh, dễ bị tổn thương", "example": "Coral reefs are delicate ecosystems.", "ipa": "/ˈdelɪkət/"},
                        {"word": "destination", "pos": "n.", "meaning": "Điểm đến, nơi ai đó hoặc thứ gì đó đang hướng tới", "example": "Costa Rica is a top ecotourism destination.", "ipa": "/ˌdestɪˈneɪʃn/"},
                        {"word": "dump", "pos": "v.", "meaning": "Vứt rác, đổ chất thải", "example": "Tourists should not dump waste in natural areas.", "ipa": "/dʌmp/"},
                        {"word": "injure", "pos": "v.", "meaning": "Gây thương tích, làm hại", "example": "Careless tourists can injure wildlife.", "ipa": "/ˈɪndʒər/"},
                        {"word": "pleasure", "pos": "n.", "meaning": "Niềm vui, sự thích thú", "example": "Ecotourism combines pleasure with conservation.", "ipa": "/ˈpleʒər/"},
                        {"word": "practice", "pos": "n.", "meaning": "Thực hành, phong tục, phương pháp", "example": "Sustainable practices are key to ecotourism.", "ipa": "/ˈpræktɪs/"},
                        {"word": "principle", "pos": "n.", "meaning": "Nguyên tắc, ý tưởng cơ bản", "example": "Leave no trace is an ecotourism principle.", "ipa": "/ˈprɪnsɪpl/"},
                        {"word": "publicity", "pos": "n.", "meaning": "Sự quảng bá, làm cho điều gì được biết đến", "example": "Ecotourism has gained positive publicity.", "ipa": "/pʌˈblɪsəti/"},
                        {"word": "recycling", "pos": "n.", "meaning": "Tái chế rác thải để sử dụng lại", "example": "Recycling is promoted in eco-lodges.", "ipa": "/ˈriːsaɪklɪŋ/"},
                        {"word": "remote", "pos": "adj.", "meaning": "Xa xôi, hẻo lánh", "example": "Ecotourism often takes place in remote areas.", "ipa": "/rɪˈmoʊt/"},
                        {"word": "strive", "pos": "v.", "meaning": "Cố gắng hết sức để đạt được", "example": "Eco-operators strive to minimize impact.", "ipa": "/straɪv/"},
                        {"word": "volunteer", "pos": "v.", "meaning": "Tình nguyện, tự nguyện làm việc không công", "example": "Tourists volunteer to clean up beaches.", "ipa": "/ˌvɒlənˈtɪər/"},
                        {"word": "wary", "pos": "adj.", "meaning": "Thận trọng, không hoàn toàn tin tưởng", "example": "Be wary of false ecotourism claims.", "ipa": "/ˈweəri/"},
                        {"word": "wilderness", "pos": "n.", "meaning": "Vùng hoang dã, thiên nhiên xa thành phố", "example": "Ecotourism explores pristine wilderness areas.", "ipa": "/ˈwɪldənəs/"}
                    ]
                },
                {
                    "name": "Learning Vacations",
                    "words": [
                        {"word": "acquire", "pos": "v.", "meaning": "Học được, có được kỹ năng", "example": "Travelers acquire new skills on learning vacations.", "ipa": "/əˈkwaɪər/"},
                        {"word": "breeze", "pos": "n.", "meaning": "Gió nhẹ", "example": "A warm breeze greeted us at the resort.", "ipa": "/briːz/"},
                        {"word": "broad", "pos": "adj.", "meaning": "Rộng lớn, đa dạng", "example": "Learning vacations offer a broad range of courses.", "ipa": "/brɔːd/"},
                        {"word": "budget", "pos": "n.", "meaning": "Ngân sách, kế hoạch chi tiêu", "example": "Set a budget before booking your vacation.", "ipa": "/ˈbʌdʒɪt/"},
                        {"word": "colorful", "pos": "adj.", "meaning": "Thú vị, đặc sắc", "example": "The market was a colorful, lively experience.", "ipa": "/ˈkʌlərfl/"},
                        {"word": "content", "pos": "n.", "meaning": "Nội dung, chủ đề", "example": "The course content focused on local cuisine.", "ipa": "/ˈkɒntent/"},
                        {"word": "costly", "pos": "adj.", "meaning": "Đắt tiền, tốn kém", "example": "Some learning vacations are costly.", "ipa": "/ˈkɒstli/"},
                        {"word": "cuisine", "pos": "n.", "meaning": "Phong cách nấu ăn, ẩm thực", "example": "The tour featured Thai cuisine lessons.", "ipa": "/kwɪˈziːn/"},
                        {"word": "economical", "pos": "adj.", "meaning": "Tiết kiệm, không đắt", "example": "Group tours are more economical.", "ipa": "/ˌiːkəˈnɒmɪkl/"},
                        {"word": "endeavor", "pos": "n.", "meaning": "Nỗ lực, hoạt động có mục đích cụ thể", "example": "Language learning is a rewarding endeavor.", "ipa": "/ɪnˈdevər/"},
                        {"word": "enroll", "pos": "v.", "meaning": "Đăng ký tham gia khóa học", "example": "Students enroll in cooking classes abroad.", "ipa": "/ɪnˈroʊl/"},
                        {"word": "hone", "pos": "v.", "meaning": "Mài giũa, cải thiện kỹ năng", "example": "The trip helped hone my photography skills.", "ipa": "/hoʊn/"},
                        {"word": "ingredient", "pos": "n.", "meaning": "Nguyên liệu trong công thức nấu ăn", "example": "Local ingredients are used in cooking classes.", "ipa": "/ɪnˈɡriːdiənt/"},
                        {"word": "ongoing", "pos": "adj.", "meaning": "Đang tiếp tục, không dừng lại", "example": "Ongoing workshops keep the experience fresh.", "ipa": "/ˈɒnɡoʊɪŋ/"},
                        {"word": "residential", "pos": "adj.", "meaning": "Liên quan đến chỗ ở, có nhà ở đi kèm", "example": "Residential courses include meals and lodging.", "ipa": "/ˌrezɪˈdenʃl/"},
                        {"word": "resort", "pos": "n.", "meaning": "Khu nghỉ dưỡng, địa điểm du lịch", "example": "The resort offered both relaxation and learning.", "ipa": "/rɪˈzɔːrt/"},
                        {"word": "sponsor", "pos": "v.", "meaning": "Tổ chức, chịu trách nhiệm điều hành", "example": "Universities sponsor archaeological digs.", "ipa": "/ˈspɒnsər/"},
                        {"word": "supervision", "pos": "n.", "meaning": "Sự giám sát, hướng dẫn", "example": "Students work under expert supervision.", "ipa": "/ˌsuːpərˈvɪʒn/"},
                        {"word": "survey", "pos": "n.", "meaning": "Khảo sát ý kiến của mẫu dân số", "example": "A survey revealed learning vacation trends.", "ipa": "/ˈsɜːrveɪ/"},
                        {"word": "taste", "pos": "n.", "meaning": "Sở thích, ưu tiên", "example": "Learning vacations suit all tastes.", "ipa": "/teɪst/"}
                    ]
                }
            ]
        },
        {
            "id": 7,
            "name": "Business",
            "color": "#b7e4c7",
            "topics": [
                {
                    "name": "Small Business Success",
                    "words": [
                        {"word": "afloat", "pos": "adj.", "meaning": "Có đủ tiền để trả nợ, không bị phá sản", "example": "Small businesses struggle to stay afloat.", "ipa": "/əˈfloʊt/"},
                        {"word": "characteristic", "pos": "n.", "meaning": "Đặc điểm, tính chất riêng biệt", "example": "Passion is a key characteristic of entrepreneurs.", "ipa": "/ˌkærɪktəˈrɪstɪk/"},
                        {"word": "compete", "pos": "v.", "meaning": "Cạnh tranh với người khác", "example": "Small businesses compete with large corporations.", "ipa": "/kəmˈpiːt/"},
                        {"word": "edge", "pos": "n.", "meaning": "Lợi thế, điểm mạnh hơn đối thủ", "example": "Good service gives businesses a competitive edge.", "ipa": "/edʒ/"},
                        {"word": "financial", "pos": "adj.", "meaning": "Liên quan đến tài chính, tiền bạc", "example": "Good financial planning is essential.", "ipa": "/faɪˈnænʃl/"},
                        {"word": "inevitably", "pos": "adv.", "meaning": "Chắc chắn, không thể tránh được", "example": "Some businesses will inevitably fail.", "ipa": "/ɪnˈevɪtəbli/"},
                        {"word": "initial", "pos": "adj.", "meaning": "Ban đầu, đầu tiên", "example": "Initial costs are high for new businesses.", "ipa": "/ɪˈnɪʃl/"},
                        {"word": "motivation", "pos": "n.", "meaning": "Động lực, lý do thúc đẩy làm điều gì", "example": "Passion is a key motivation for entrepreneurs.", "ipa": "/ˌmoʊtɪˈveɪʃn/"},
                        {"word": "niche", "pos": "n.", "meaning": "Vị trí thị trường phù hợp, thị trường ngách", "example": "Finding a niche market is crucial.", "ipa": "/niːʃ/"},
                        {"word": "particular", "pos": "adj.", "meaning": "Cụ thể, riêng biệt", "example": "Each customer has particular preferences.", "ipa": "/pərˈtɪkjələr/"},
                        {"word": "personalized", "pos": "adj.", "meaning": "Được cá nhân hóa, làm riêng cho từng người", "example": "Personalized service builds loyalty.", "ipa": "/ˈpɜːrsənəlaɪzd/"},
                        {"word": "potential", "pos": "adj.", "meaning": "Tiềm năng, có thể xảy ra", "example": "Every customer is a potential repeat buyer.", "ipa": "/pəˈtenʃl/"},
                        {"word": "product", "pos": "n.", "meaning": "Sản phẩm được sản xuất", "example": "A quality product builds reputation.", "ipa": "/ˈprɒdʌkt/"},
                        {"word": "profit", "pos": "n.", "meaning": "Lợi nhuận sau khi trừ chi phí", "example": "Small businesses often have low profit margins.", "ipa": "/ˈprɒfɪt/"},
                        {"word": "project", "pos": "v.", "meaning": "Ước tính, dự báo số liệu tương lai", "example": "Owners project next year's revenue.", "ipa": "/prəˈdʒekt/"},
                        {"word": "reputation", "pos": "n.", "meaning": "Danh tiếng, ý kiến chung về ai đó", "example": "A good reputation attracts customers.", "ipa": "/ˌrepjəˈteɪʃn/"},
                        {"word": "sound", "pos": "adj.", "meaning": "Lành mạnh, không có rủi ro tài chính", "example": "Sound financial planning prevents failure.", "ipa": "/saʊnd/"},
                        {"word": "tip", "pos": "n.", "meaning": "Lời khuyên, gợi ý hữu ích", "example": "Business experts share tips for success.", "ipa": "/tɪp/"},
                        {"word": "unique", "pos": "adj.", "meaning": "Độc đáo, khác biệt với tất cả những thứ khác", "example": "A unique product stands out in the market.", "ipa": "/juːˈniːk/"},
                        {"word": "vital", "pos": "adj.", "meaning": "Quan trọng, thiết yếu cho thành công", "example": "Customer service is vital for small businesses.", "ipa": "/ˈvaɪtl/"}
                    ]
                },
                {
                    "name": "Brand Loyalty",
                    "words": [
                        {"word": "bond", "pos": "n.", "meaning": "Sự kết nối, mối liên hệ mạnh mẽ", "example": "Brand loyalty creates a psychological bond.", "ipa": "/bɒnd/"},
                        {"word": "brand", "pos": "n.", "meaning": "Thương hiệu, tên công ty của sản phẩm", "example": "Consumers trust well-known brands.", "ipa": "/brænd/"},
                        {"word": "burgeoning", "pos": "adj.", "meaning": "Đang phát triển nhanh chóng", "example": "There is a burgeoning market for organic food.", "ipa": "/ˈbɜːrdʒənɪŋ/"},
                        {"word": "conglomerate", "pos": "n.", "meaning": "Tập đoàn lớn sở hữu nhiều công ty nhỏ", "example": "The conglomerate owns dozens of brands.", "ipa": "/kənˈɡlɒmərət/"},
                        {"word": "consistently", "pos": "adv.", "meaning": "Thường xuyên, luôn luôn như vậy", "example": "Loyal customers consistently choose one brand.", "ipa": "/kənˈsɪstəntli/"},
                        {"word": "convince", "pos": "v.", "meaning": "Thuyết phục ai đó tin hoặc làm gì", "example": "Advertising convinces customers to buy.", "ipa": "/kənˈvɪns/"},
                        {"word": "endorsement", "pos": "n.", "meaning": "Sự ủng hộ công khai", "example": "Celebrity endorsement boosts brand loyalty.", "ipa": "/ɪnˈdɔːrsmənt/"},
                        {"word": "fleeting", "pos": "adj.", "meaning": "Thoáng qua, kết thúc nhanh chóng", "example": "Some brand preferences are fleeting.", "ipa": "/ˈfliːtɪŋ/"},
                        {"word": "ignore", "pos": "v.", "meaning": "Bỏ qua, không chú ý đến", "example": "Loyal customers ignore competitor ads.", "ipa": "/ɪɡˈnɔːr/"},
                        {"word": "loyalty", "pos": "n.", "meaning": "Lòng trung thành, niềm tin vào điều gì", "example": "Customer loyalty is worth more than advertising.", "ipa": "/ˈlɔɪəlti/"},
                        {"word": "outperform", "pos": "v.", "meaning": "Thực hiện tốt hơn đối thủ", "example": "Loyal customers believe their brand outperforms others.", "ipa": "/ˌaʊtpərˈfɔːrm/"},
                        {"word": "passion", "pos": "n.", "meaning": "Niềm đam mê mạnh mẽ", "example": "Apple fans have a passion for the brand.", "ipa": "/ˈpæʃn/"},
                        {"word": "phenomenon", "pos": "n.", "meaning": "Hiện tượng đặc biệt, điều bất thường xảy ra", "example": "Brand loyalty is a global phenomenon.", "ipa": "/fɪˈnɒmɪnən/"},
                        {"word": "prevail", "pos": "v.", "meaning": "Thịnh hành, chiếm ưu thế", "example": "Brand loyalty prevails in developed markets.", "ipa": "/prɪˈveɪl/"},
                        {"word": "promote", "pos": "v.", "meaning": "Quảng cáo, xúc tiến", "example": "Companies promote loyalty through rewards.", "ipa": "/prəˈmoʊt/"},
                        {"word": "reverse", "pos": "v.", "meaning": "Đảo ngược, thay đổi thành điều trái ngược", "example": "It is hard to reverse brand loyalty.", "ipa": "/rɪˈvɜːrs/"},
                        {"word": "selective", "pos": "adj.", "meaning": "Chọn lọc, có mục đích chọn cái này không chọn cái kia", "example": "Loyal customers are selective about products.", "ipa": "/sɪˈlektɪv/"},
                        {"word": "staple", "pos": "n.", "meaning": "Mặt hàng thiết yếu trong gia đình", "example": "Bread and milk are household staples.", "ipa": "/ˈsteɪpl/"},
                        {"word": "status", "pos": "n.", "meaning": "Vị thế xã hội, địa vị", "example": "Luxury brands convey status.", "ipa": "/ˈsteɪtəs/"},
                        {"word": "thirst", "pos": "n.", "meaning": "Khao khát mạnh mẽ về điều gì", "example": "Consumers have a thirst for new technology.", "ipa": "/θɜːrst/"}
                    ]
                },
                {
                    "name": "Global Outsourcing",
                    "words": [
                        {"word": "boon", "pos": "n.", "meaning": "Lợi ích, điều có lợi", "example": "Outsourcing is a boon for developing economies.", "ipa": "/buːn/"},
                        {"word": "branch", "pos": "n.", "meaning": "Chi nhánh địa phương của công ty lớn", "example": "The company opened a branch overseas.", "ipa": "/brɑːntʃ/"},
                        {"word": "catch up", "pos": "v.", "meaning": "Đuổi kịp người hoặc vật đang ở phía trước", "example": "Developing nations catch up economically.", "ipa": "/kætʃ ʌp/"},
                        {"word": "coincide", "pos": "v.", "meaning": "Xảy ra cùng lúc", "example": "Outsourcing growth coincides with globalization.", "ipa": "/ˌkoʊɪnˈsaɪd/"},
                        {"word": "confront", "pos": "v.", "meaning": "Đối mặt với khó khăn", "example": "Companies confront challenges when outsourcing.", "ipa": "/kənˈfrʌnt/"},
                        {"word": "controversy", "pos": "n.", "meaning": "Tranh cãi, sự bất đồng ảnh hưởng nhiều người", "example": "Outsourcing has sparked controversy.", "ipa": "/ˈkɒntrəvɜːrsi/"},
                        {"word": "decisive", "pos": "adj.", "meaning": "Quyết định, có tầm quan trọng ảnh hưởng đến quyết định", "example": "Cost savings are a decisive factor.", "ipa": "/dɪˈsaɪsɪv/"},
                        {"word": "enticing", "pos": "adj.", "meaning": "Hấp dẫn, thu hút", "example": "Low wages make outsourcing enticing.", "ipa": "/ɪnˈtaɪsɪŋ/"},
                        {"word": "epicenter", "pos": "n.", "meaning": "Trung tâm, điểm trọng tâm nhất", "example": "India is the epicenter of IT outsourcing.", "ipa": "/ˈepɪsentər/"},
                        {"word": "firm", "pos": "n.", "meaning": "Công ty, doanh nghiệp", "example": "Many firms outsource customer service.", "ipa": "/fɜːrm/"},
                        {"word": "looming", "pos": "adj.", "meaning": "Đang đến gần, thường là mối đe dọa", "example": "Looming regulations may affect outsourcing.", "ipa": "/ˈluːmɪŋ/"},
                        {"word": "opponent", "pos": "n.", "meaning": "Người phản đối, người không đồng ý", "example": "Opponents of outsourcing cite job losses.", "ipa": "/əˈpoʊnənt/"},
                        {"word": "point", "pos": "v.", "meaning": "Gọi sự chú ý đến", "example": "Critics point to negative effects.", "ipa": "/pɔɪnt/"},
                        {"word": "preponderance", "pos": "n.", "meaning": "Số lượng lớn nhất, chiếm đa số", "example": "A preponderance of firms support outsourcing.", "ipa": "/prɪˈpɒndərəns/"},
                        {"word": "proponent", "pos": "n.", "meaning": "Người ủng hộ, người bênh vực", "example": "Proponents say outsourcing benefits all.", "ipa": "/prəˈpoʊnənt/"},
                        {"word": "remainder", "pos": "n.", "meaning": "Phần còn lại", "example": "The remainder of the work stayed in-house.", "ipa": "/rɪˈmeɪndər/"},
                        {"word": "routinely", "pos": "adv.", "meaning": "Thường xuyên, theo thói quen", "example": "Companies routinely outsource IT support.", "ipa": "/ruːˈtiːnli/"},
                        {"word": "shift", "pos": "n.", "meaning": "Ca làm việc, khoảng thời gian làm việc", "example": "Night shift workers handled overseas tasks.", "ipa": "/ʃɪft/"},
                        {"word": "turnover", "pos": "n.", "meaning": "Tỷ lệ nhân viên rời đi và được thay thế", "example": "High turnover is common in outsourced jobs.", "ipa": "/ˈtɜːrnoʊvər/"},
                        {"word": "wealthy", "pos": "adj.", "meaning": "Giàu có", "example": "Wealthy nations outsource to reduce costs.", "ipa": "/ˈwelθi/"}
                    ]
                }
            ]
        },
        {
            "id": 8,
            "name": "Society",
            "color": "#d8f3dc",
            "topics": [
                {
                    "name": "Social Networking",
                    "words": [
                        {"word": "acquaintance", "pos": "n.", "meaning": "Người quen không thân thiết", "example": "Online, we have many acquaintances.", "ipa": "/əˈkweɪntəns/"},
                        {"word": "adolescent", "pos": "n.", "meaning": "Người trong độ tuổi thiếu niên 13-19", "example": "Adolescents spend hours on social media.", "ipa": "/ˌædəˈlesnt/"},
                        {"word": "apparently", "pos": "adv.", "meaning": "Có vẻ như, theo như có vẻ thấy", "example": "Social media is apparently here to stay.", "ipa": "/əˈpærəntli/"},
                        {"word": "carry out", "pos": "v.", "meaning": "Thực hiện, tiến hành", "example": "Researchers carry out studies on social media.", "ipa": "/ˈkæri aʊt/"},
                        {"word": "community", "pos": "n.", "meaning": "Cộng đồng, nhóm xã hội", "example": "Online communities connect people globally.", "ipa": "/kəˈmjuːnəti/"},
                        {"word": "consequence", "pos": "n.", "meaning": "Hậu quả, kết quả", "example": "Cyberbullying has serious consequences.", "ipa": "/ˈkɒnsɪkwəns/"},
                        {"word": "contact", "pos": "n.", "meaning": "Liên lạc, kết nối, giao tiếp", "example": "Social media keeps us in contact.", "ipa": "/ˈkɒntækt/"},
                        {"word": "eradicate", "pos": "v.", "meaning": "Xóa bỏ hoàn toàn", "example": "We cannot eradicate social media's influence.", "ipa": "/ɪˈrædɪkeɪt/"},
                        {"word": "exchange", "pos": "v.", "meaning": "Trao đổi, đổi lấy nhau", "example": "People exchange ideas online.", "ipa": "/ɪksˈtʃeɪndʒ/"},
                        {"word": "explode", "pos": "v.", "meaning": "Bùng nổ, phát triển đột ngột và nhanh chóng", "example": "Social media use has exploded globally.", "ipa": "/ɪkˈsploʊd/"},
                        {"word": "immense", "pos": "adj.", "meaning": "Khổng lồ, rất lớn", "example": "Social media has immense influence.", "ipa": "/ɪˈmens/"},
                        {"word": "impose", "pos": "v.", "meaning": "Áp đặt, bắt buộc", "example": "Parents impose limits on screen time.", "ipa": "/ɪmˈpoʊz/"},
                        {"word": "interact", "pos": "v.", "meaning": "Giao tiếp, tương tác với nhau", "example": "People interact online more than ever.", "ipa": "/ˌɪntərˈækt/"},
                        {"word": "post", "pos": "v.", "meaning": "Đăng thông tin lên nơi công cộng", "example": "Users post updates on social media.", "ipa": "/poʊst/"},
                        {"word": "pursue", "pos": "v.", "meaning": "Theo đuổi, tìm kiếm", "example": "People pursue connections online.", "ipa": "/pərˈsjuː/"},
                        {"word": "statistics", "pos": "n.", "meaning": "Thống kê, thông tin dưới dạng số liệu", "example": "Statistics show social media use is rising.", "ipa": "/stəˈtɪstɪks/"},
                        {"word": "susceptible", "pos": "adj.", "meaning": "Dễ bị ảnh hưởng, nhạy cảm", "example": "Young people are susceptible to peer pressure.", "ipa": "/səˈseptɪbl/"},
                        {"word": "trend", "pos": "n.", "meaning": "Xu hướng, mốt phổ biến", "example": "Viral content sets social media trends.", "ipa": "/trend/"},
                        {"word": "undergo", "pos": "v.", "meaning": "Trải qua, chịu đựng điều khó khăn", "example": "Society has undergone rapid change.", "ipa": "/ˌʌndərˈɡoʊ/"},
                        {"word": "unfold", "pos": "v.", "meaning": "Phát triển, mở ra theo thời gian", "example": "Events unfold quickly on social media.", "ipa": "/ˌʌnˈfoʊld/"}
                    ]
                },
                {
                    "name": "Why Are Women Leaving Science Careers?",
                    "words": [
                        {"word": "absence", "pos": "n.", "meaning": "Sự vắng mặt, thời gian không có mặt", "example": "Absence due to maternity affects careers.", "ipa": "/ˈæbsəns/"},
                        {"word": "academic", "pos": "adj.", "meaning": "Liên quan đến trường học, nhất là đại học", "example": "Academic careers require long hours.", "ipa": "/ˌækəˈdemɪk/"},
                        {"word": "approximately", "pos": "adv.", "meaning": "Khoảng, gần đúng", "example": "Approximately 50% of women leave science.", "ipa": "/əˈprɒksɪmətli/"},
                        {"word": "bear", "pos": "v.", "meaning": "Gánh chịu trách nhiệm", "example": "Women often bear a greater family burden.", "ipa": "/beər/"},
                        {"word": "commensurate", "pos": "adj.", "meaning": "Tương xứng, bằng nhau về quy mô", "example": "Pay should be commensurate with experience.", "ipa": "/kəˈmenʃərət/"},
                        {"word": "devote", "pos": "v.", "meaning": "Cống hiến, dành thời gian công sức", "example": "Women devote more time to family care.", "ipa": "/dɪˈvoʊt/"},
                        {"word": "dire", "pos": "adj.", "meaning": "Rất nghiêm trọng, cực kỳ tệ", "example": "The loss of women in science has dire consequences.", "ipa": "/daɪər/"},
                        {"word": "discrepancy", "pos": "n.", "meaning": "Sự chênh lệch, sự không nhất quán", "example": "There is a discrepancy in pay between genders.", "ipa": "/dɪˈskrepənsi/"},
                        {"word": "equality", "pos": "n.", "meaning": "Bình đẳng, quyền và cơ hội như nhau", "example": "Gender equality in science is essential.", "ipa": "/ɪˈkwɒləti/"},
                        {"word": "frustration", "pos": "n.", "meaning": "Sự thất vọng, cảm giác không đạt được mục tiêu", "example": "Women experience frustration in male-dominated fields.", "ipa": "/frʌˈstreɪʃn/"},
                        {"word": "funding", "pos": "n.", "meaning": "Tài trợ tài chính", "example": "Women scientists receive less funding.", "ipa": "/ˈfʌndɪŋ/"},
                        {"word": "guidance", "pos": "n.", "meaning": "Lời khuyên, sự hỗ trợ định hướng", "example": "Mentors provide guidance to young scientists.", "ipa": "/ˈɡaɪdəns/"},
                        {"word": "inordinate", "pos": "adj.", "meaning": "Quá mức, nhiều hơn mức hợp lý", "example": "Women face inordinate pressure in academia.", "ipa": "/ɪnˈɔːrdɪnət/"},
                        {"word": "invaluable", "pos": "adj.", "meaning": "Vô giá, cực kỳ hữu ích", "example": "Women's contributions to science are invaluable.", "ipa": "/ɪnˈvæljuəbl/"},
                        {"word": "mentor", "pos": "n.", "meaning": "Người cố vấn, người cho lời khuyên và hỗ trợ", "example": "A mentor helped her navigate her career.", "ipa": "/ˈmentɔːr/"},
                        {"word": "persist", "pos": "v.", "meaning": "Tiếp tục, kiên trì không bỏ cuộc", "example": "Few women persist in science to senior roles.", "ipa": "/pərˈsɪst/"},
                        {"word": "pressure", "pos": "n.", "meaning": "Áp lực, đòi hỏi, trách nhiệm", "example": "Work-life pressure drives women away.", "ipa": "/ˈpreʃər/"},
                        {"word": "progress", "pos": "v.", "meaning": "Tiến lên, phát triển về phía trước", "example": "Women progress more slowly in science.", "ipa": "/prəˈɡres/"},
                        {"word": "struggle", "pos": "v.", "meaning": "Đấu tranh, vật lộn với khó khăn", "example": "Women struggle for recognition in science.", "ipa": "/ˈstrʌɡl/"},
                        {"word": "validate", "pos": "v.", "meaning": "Công nhận, làm cho ai đó cảm thấy được trân trọng", "example": "Mentors validate women's scientific contributions.", "ipa": "/ˈvælɪdeɪt/"}
                    ]
                },
                {
                    "name": "Wheelchair-Accessibility Issues",
                    "words": [
                        {"word": "abound", "pos": "v.", "meaning": "Tồn tại với số lượng lớn, phổ biến rộng rãi", "example": "Accessibility challenges abound in old buildings.", "ipa": "/əˈbaʊnd/"},
                        {"word": "account for", "pos": "v.", "meaning": "Chịu trách nhiệm, là nguyên nhân của", "example": "Poor design accounts for many barriers.", "ipa": "/əˈkaʊnt fɔːr/"},
                        {"word": "capable", "pos": "adj.", "meaning": "Có khả năng làm điều gì", "example": "Wheelchair users are capable of independent living.", "ipa": "/ˈkeɪpəbl/"},
                        {"word": "compact", "pos": "adj.", "meaning": "Nhỏ gọn", "example": "Compact wheelchairs fit in smaller spaces.", "ipa": "/ˈkɒmpækt/"},
                        {"word": "corridor", "pos": "n.", "meaning": "Hành lang, lối đi trong tòa nhà", "example": "Wide corridors allow wheelchair access.", "ipa": "/ˈkɒrɪdɔːr/"},
                        {"word": "curb", "pos": "n.", "meaning": "Lề đường, cạnh nổi cao của vỉa hè", "example": "Curb cuts help wheelchair users cross streets.", "ipa": "/kɜːrb/"},
                        {"word": "disability", "pos": "n.", "meaning": "Khuyết tật, tình trạng khiến khó làm điều bình thường", "example": "Millions live with a physical disability.", "ipa": "/ˌdɪsəˈbɪləti/"},
                        {"word": "exterior", "pos": "n.", "meaning": "Bên ngoài, mặt ngoài của thứ gì", "example": "Building exteriors must have ramps.", "ipa": "/ɪkˈstɪəriər/"},
                        {"word": "incapacitated", "pos": "adj.", "meaning": "Bị mất khả năng làm việc bình thường", "example": "Incapacitated individuals need accessible spaces.", "ipa": "/ɪnkəˈpæsɪteɪtɪd/"},
                        {"word": "interior", "pos": "n.", "meaning": "Bên trong, phần nội thất của thứ gì", "example": "Building interiors must be wheelchair friendly.", "ipa": "/ɪnˈtɪəriər/"},
                        {"word": "necessitate", "pos": "v.", "meaning": "Làm cần thiết, đòi hỏi", "example": "Disability necessitates accessible design.", "ipa": "/nəˈsesɪteɪt/"},
                        {"word": "poverty", "pos": "n.", "meaning": "Tình trạng nghèo đói", "example": "Poverty prevents access to quality wheelchairs.", "ipa": "/ˈpɒvəti/"},
                        {"word": "ramp", "pos": "n.", "meaning": "Đường dốc nối hai mức độ cao khác nhau", "example": "A ramp allows wheelchair access to buildings.", "ipa": "/ræmp/"},
                        {"word": "recreation", "pos": "n.", "meaning": "Hoạt động giải trí, vui chơi", "example": "Recreation areas must be accessible.", "ipa": "/ˌrekriˈeɪʃn/"},
                        {"word": "slippery", "pos": "adj.", "meaning": "Trơn trượt, khó đứng hay giữ chặt", "example": "Slippery floors are dangerous for wheelchair users.", "ipa": "/ˈslɪpəri/"},
                        {"word": "slope", "pos": "n.", "meaning": "Mặt nghiêng, dốc từ cao xuống thấp", "example": "A gentle slope is easier to navigate.", "ipa": "/sloʊp/"},
                        {"word": "switch", "pos": "n.", "meaning": "Công tắc, nút bật tắt máy móc", "example": "Switches must be low enough for wheelchair users.", "ipa": "/swɪtʃ/"},
                        {"word": "terrain", "pos": "n.", "meaning": "Địa hình, bề mặt đất", "example": "Rough terrain is difficult for wheelchairs.", "ipa": "/təˈreɪn/"},
                        {"word": "unwieldy", "pos": "adj.", "meaning": "Khó kiểm soát, bất tiện", "example": "Large wheelchairs can be unwieldy indoors.", "ipa": "/ʌnˈwiːldi/"},
                        {"word": "update", "pos": "v.", "meaning": "Hiện đại hóa, cải thiện", "example": "Old buildings need to be updated for accessibility.", "ipa": "/ˈʌpdeɪt/"}
                    ]
                }
            ]
        },
        {
            "id": 9,
            "name": "Education",
            "color": "#b7e4c7",
            "topics": [
                {
                    "name": "Learning Styles",
                    "words": [
                        {"word": "approach", "pos": "n.", "meaning": "Phương pháp, cách thức tiếp cận", "example": "Teachers adapt their approach to each student.", "ipa": "/əˈproʊtʃ/"},
                        {"word": "auditory", "pos": "adj.", "meaning": "Liên quan đến thính giác, nghe", "example": "Auditory learners prefer listening to lectures.", "ipa": "/ˈɔːdɪtɔːri/"},
                        {"word": "blend", "pos": "n.", "meaning": "Sự kết hợp, hỗn hợp của nhiều thứ", "example": "Good teaching uses a blend of methods.", "ipa": "/blend/"},
                        {"word": "circumstance", "pos": "n.", "meaning": "Hoàn cảnh, tình huống", "example": "Learning style depends on circumstance.", "ipa": "/ˈsɜːrkəmstæns/"},
                        {"word": "confidence", "pos": "n.", "meaning": "Sự tự tin vào bản thân", "example": "Success builds students' confidence.", "ipa": "/ˈkɒnfɪdəns/"},
                        {"word": "conventional", "pos": "adj.", "meaning": "Thông thường, truyền thống", "example": "Conventional teaching uses lectures.", "ipa": "/kənˈvenʃənl/"},
                        {"word": "diagram", "pos": "n.", "meaning": "Sơ đồ, hình vẽ đơn giản để giải thích", "example": "Visual learners prefer diagrams.", "ipa": "/ˈdaɪəɡræm/"},
                        {"word": "dominant", "pos": "adj.", "meaning": "Chiếm ưu thế, quan trọng hơn", "example": "One learning style tends to be dominant.", "ipa": "/ˈdɒmɪnənt/"},
                        {"word": "encouragement", "pos": "n.", "meaning": "Sự khích lệ, lời khen hỗ trợ tiếp tục", "example": "Students need encouragement to succeed.", "ipa": "/ɪnˈkʌrɪdʒmənt/"},
                        {"word": "expose", "pos": "v.", "meaning": "Tạo cơ hội trải nghiệm, học điều mới", "example": "Teachers expose students to diverse methods.", "ipa": "/ɪkˈspoʊz/"},
                        {"word": "facial", "pos": "adj.", "meaning": "Liên quan đến khuôn mặt", "example": "Facial expressions help visual learners.", "ipa": "/ˈfeɪʃl/"},
                        {"word": "fidget", "pos": "v.", "meaning": "Cựa quậy, không ngồi yên vì lo lắng", "example": "Kinesthetic learners fidget during lectures.", "ipa": "/ˈfɪdʒɪt/"},
                        {"word": "hinder", "pos": "v.", "meaning": "Cản trở, ngăn cản", "example": "Poor teaching can hinder learning.", "ipa": "/ˈhɪndər/"},
                        {"word": "incorporate", "pos": "v.", "meaning": "Kết hợp vào, đưa vào bên trong", "example": "Teachers incorporate different learning styles.", "ipa": "/ɪnˈkɔːrpəreɪt/"},
                        {"word": "kinesthetic", "pos": "adj.", "meaning": "Liên quan đến vận động cơ thể", "example": "Kinesthetic learners learn by doing.", "ipa": "/ˌkɪnɪsˈθetɪk/"},
                        {"word": "manipulate", "pos": "v.", "meaning": "Sử dụng tay để di chuyển đồ vật", "example": "Students manipulate materials in lab work.", "ipa": "/məˈnɪpjəleɪt/"},
                        {"word": "obstruction", "pos": "n.", "meaning": "Vật cản, thứ chặn đường", "example": "Learning disabilities are an obstruction.", "ipa": "/əbˈstrʌkʃn/"},
                        {"word": "recite", "pos": "v.", "meaning": "Đọc to, lặp lại thành tiếng", "example": "Auditory learners benefit from reciting notes.", "ipa": "/rɪˈsaɪt/"},
                        {"word": "solitary", "pos": "adj.", "meaning": "Độc lập, làm một mình", "example": "Some learners prefer solitary study.", "ipa": "/ˈsɒlɪtəri/"},
                        {"word": "verbal", "pos": "adj.", "meaning": "Liên quan đến từ ngữ, lời nói", "example": "Verbal instructions suit auditory learners.", "ipa": "/ˈvɜːrbl/"}
                    ]
                },
                {
                    "name": "The Homeschool Option",
                    "words": [
                        {"word": "address", "pos": "v.", "meaning": "Giải quyết vấn đề, đối phó với vấn đề", "example": "Homeschooling addresses individual learning needs.", "ipa": "/əˈdres/"},
                        {"word": "adequately", "pos": "adv.", "meaning": "Một cách đầy đủ, đủ tốt", "example": "Parents must adequately educate their children.", "ipa": "/ˈædɪkwətli/"},
                        {"word": "alternative", "pos": "n.", "meaning": "Sự lựa chọn khác, phương án thay thế", "example": "Homeschooling is an alternative to public school.", "ipa": "/ɔːlˈtɜːrnətɪv/"},
                        {"word": "compulsory", "pos": "adj.", "meaning": "Bắt buộc, được yêu cầu", "example": "Education is compulsory in most countries.", "ipa": "/kəmˈpʌlsəri/"},
                        {"word": "concerned", "pos": "adj.", "meaning": "Lo lắng, quan tâm", "example": "Parents are concerned about school quality.", "ipa": "/kənˈsɜːrnd/"},
                        {"word": "dissatisfied", "pos": "adj.", "meaning": "Không hài lòng, chưa thỏa mãn", "example": "Dissatisfied parents choose homeschooling.", "ipa": "/dɪsˈsætɪsfaɪd/"},
                        {"word": "exceptional", "pos": "adj.", "meaning": "Đặc biệt, vượt trội hơn mức bình thường", "example": "Exceptional students may need different education.", "ipa": "/ɪkˈsepʃənl/"},
                        {"word": "instruction", "pos": "n.", "meaning": "Sự dạy học, giảng dạy", "example": "Parents provide daily instruction at home.", "ipa": "/ɪnˈstrʌkʃn/"},
                        {"word": "latter", "pos": "adj.", "meaning": "Gần cuối, thuộc về phần sau", "example": "The latter option is homeschooling.", "ipa": "/ˈlætər/"},
                        {"word": "majority", "pos": "n.", "meaning": "Phần lớn, số đông", "example": "The majority of homeschooled kids succeed.", "ipa": "/məˈdʒɒrəti/"},
                        {"word": "mandate", "pos": "v.", "meaning": "Ra lệnh chính thức, yêu cầu", "example": "The law mandates regular curriculum reporting.", "ipa": "/ˈmændeɪt/"},
                        {"word": "novel", "pos": "adj.", "meaning": "Mới lạ, chưa từng thấy trước đây", "example": "Homeschooling was once a novel concept.", "ipa": "/ˈnɒvl/"},
                        {"word": "obligatory", "pos": "adj.", "meaning": "Bắt buộc, phải làm theo yêu cầu", "example": "Curriculum testing may be obligatory.", "ipa": "/əˈblɪɡətɔːri/"},
                        {"word": "periodic", "pos": "adj.", "meaning": "Định kỳ, lặp đi lặp lại đều đặn", "example": "Periodic assessments check progress.", "ipa": "/ˌpɪəriˈɒdɪk/"},
                        {"word": "philosophy", "pos": "n.", "meaning": "Triết học, hệ thống niềm tin và giá trị", "example": "Each family has a different education philosophy.", "ipa": "/fɪˈlɒsəfi/"},
                        {"word": "prior", "pos": "adj.", "meaning": "Trước, có trước", "example": "Prior experience in teaching helps parents.", "ipa": "/ˈpraɪər/"},
                        {"word": "relatively", "pos": "adv.", "meaning": "Tương đối, so với thứ khác", "example": "Homeschooling is relatively flexible.", "ipa": "/ˈrelətɪvli/"},
                        {"word": "tutor", "pos": "n.", "meaning": "Gia sư, người dạy kèm riêng", "example": "Some families hire a tutor for extra help.", "ipa": "/ˈtjuːtər/"},
                        {"word": "vast", "pos": "adj.", "meaning": "Rộng lớn, đồ sộ", "example": "A vast amount of resources exists online.", "ipa": "/vɑːst/"},
                        {"word": "widespread", "pos": "adj.", "meaning": "Phổ biến rộng rãi, lan rộng khắp nơi", "example": "Homeschooling is becoming widespread.", "ipa": "/ˈwaɪdspred/"}
                    ]
                },
                {
                    "name": "Educating the Gifted",
                    "words": [
                        {"word": "assess", "pos": "v.", "meaning": "Đánh giá, đo lường năng lực", "example": "Teachers assess students' abilities regularly.", "ipa": "/əˈses/"},
                        {"word": "constructive", "pos": "adj.", "meaning": "Tích cực, có lợi và hỗ trợ", "example": "Constructive feedback helps gifted students.", "ipa": "/kənˈstrʌktɪv/"},
                        {"word": "curriculum", "pos": "n.", "meaning": "Chương trình học, các môn học ở trường", "example": "Gifted students need an enriched curriculum.", "ipa": "/kəˈrɪkjələm/"},
                        {"word": "dedicate", "pos": "v.", "meaning": "Cống hiến, dành tâm huyết", "example": "Schools dedicate resources to gifted programs.", "ipa": "/ˈdedɪkeɪt/"},
                        {"word": "discipline", "pos": "n.", "meaning": "Kỷ luật, sự duy trì hành vi đúng mực", "example": "Gifted students still need discipline.", "ipa": "/ˈdɪsɪplɪn/"},
                        {"word": "enriched", "pos": "adj.", "meaning": "Được nâng cao, chất lượng cao hơn", "example": "An enriched program challenges gifted learners.", "ipa": "/ɪnˈrɪtʃt/"},
                        {"word": "extraordinary", "pos": "adj.", "meaning": "Phi thường, đặc biệt", "example": "Gifted children show extraordinary abilities.", "ipa": "/ɪkˈstrɔːrdɪnəri/"},
                        {"word": "gifted", "pos": "adj.", "meaning": "Có tài năng đặc biệt", "example": "Gifted students learn faster than peers.", "ipa": "/ˈɡɪftɪd/"},
                        {"word": "inquisitiveness", "pos": "n.", "meaning": "Sự ham muốn hiểu biết, tính tò mò", "example": "Inquisitiveness is a sign of giftedness.", "ipa": "/ɪnˈkwɪzɪtɪvnəs/"},
                        {"word": "interpretation", "pos": "n.", "meaning": "Sự hiểu biết, cách lý giải", "example": "Gifted students develop their own interpretations.", "ipa": "/ɪnˌtɜːrprɪˈteɪʃn/"},
                        {"word": "moderately", "pos": "adv.", "meaning": "Ở mức độ vừa phải, không quá mức", "example": "Most students are only moderately gifted.", "ipa": "/ˈmɒdərətli/"},
                        {"word": "peer", "pos": "n.", "meaning": "Bạn đồng trang lứa, người cùng cấp độ", "example": "Gifted students need peers at the same level.", "ipa": "/pɪər/"},
                        {"word": "profoundly", "pos": "adv.", "meaning": "Sâu sắc, mức độ rất cao", "example": "Some children are profoundly gifted.", "ipa": "/prəˈfaʊndli/"},
                        {"word": "recognize", "pos": "v.", "meaning": "Nhận biết, xác định", "example": "Schools must recognize gifted children.", "ipa": "/ˈrekəɡnaɪz/"},
                        {"word": "remedial", "pos": "adj.", "meaning": "Bù đắp, chương trình hỗ trợ học sinh yếu", "example": "Remedial education helps struggling students.", "ipa": "/rɪˈmiːdiəl/"},
                        {"word": "simultaneous", "pos": "adj.", "meaning": "Đồng thời, xảy ra cùng một lúc", "example": "Gifted students process information simultaneously.", "ipa": "/ˌsɪmlˈteɪniəs/"},
                        {"word": "sophisticated", "pos": "adj.", "meaning": "Tinh vi, phức tạp và nâng cao", "example": "Gifted students prefer sophisticated material.", "ipa": "/səˈfɪstɪkeɪtɪd/"},
                        {"word": "transfer", "pos": "v.", "meaning": "Chuyển giao, di chuyển từ nơi này sang nơi khác", "example": "Gifted students transfer skills across subjects.", "ipa": "/ˈtrænsfɜːr/"},
                        {"word": "turn into", "pos": "v.", "meaning": "Trở thành, biến thành", "example": "Curiosity can turn into brilliance.", "ipa": "/tɜːrn ˈɪntə/"},
                        {"word": "withdrawal", "pos": "n.", "meaning": "Sự không muốn tham gia, rút lui", "example": "Withdrawal from class is common in gifted students.", "ipa": "/wɪðˈdrɔːəl/"}
                    ]
                }
            ]
        },
        {
            "id": 10,
            "name": "Technology/Inventions",
            "color": "#95d5b2",
            "topics": [
                {
                    "name": "Development of the Lightbulb",
                    "words": [
                        {"word": "back", "pos": "v.", "meaning": "Ủng hộ, hỗ trợ về tài chính", "example": "Investors backed Edison's research.", "ipa": "/bæk/"},
                        {"word": "clamp", "pos": "v.", "meaning": "Kẹp chặt, giữ chắc", "example": "The filament was clamped into the bulb.", "ipa": "/klæmp/"},
                        {"word": "critical", "pos": "adj.", "meaning": "Cực kỳ quan trọng", "example": "The right filament was critical to success.", "ipa": "/ˈkrɪtɪkl/"},
                        {"word": "current", "pos": "n.", "meaning": "Dòng điện, nước hoặc không khí chảy", "example": "Electric current powers the lightbulb.", "ipa": "/ˈkɜːrənt/"},
                        {"word": "derive", "pos": "v.", "meaning": "Lấy từ, xuất phát từ nguồn khác", "example": "The design was derived from earlier prototypes.", "ipa": "/dɪˈraɪv/"},
                        {"word": "device", "pos": "n.", "meaning": "Thiết bị, công cụ máy móc", "example": "The lightbulb was a revolutionary device.", "ipa": "/dɪˈvaɪs/"},
                        {"word": "entrepreneur", "pos": "n.", "meaning": "Doanh nhân, người khởi nghiệp kinh doanh", "example": "Edison was a prolific entrepreneur.", "ipa": "/ˌɒntrəprəˈnɜːr/"},
                        {"word": "file", "pos": "v.", "meaning": "Nộp hồ sơ chính thức, ghi lại chính thức", "example": "Edison filed over 1000 patents.", "ipa": "/faɪl/"},
                        {"word": "infringement", "pos": "n.", "meaning": "Hành vi vi phạm quy tắc hoặc luật pháp", "example": "Patent infringement led to lawsuits.", "ipa": "/ɪnˈfrɪndʒmənt/"},
                        {"word": "inspiration", "pos": "n.", "meaning": "Nguồn cảm hứng, ý tưởng đột ngột sáng tạo", "example": "Nature was a major inspiration for inventors.", "ipa": "/ˌɪnspəˈreɪʃn/"},
                        {"word": "invalid", "pos": "adj.", "meaning": "Không hợp lệ, không hợp pháp", "example": "The patent was declared invalid.", "ipa": "/ɪnˈvælɪd/"},
                        {"word": "inventor", "pos": "n.", "meaning": "Nhà phát minh, người tạo ra thứ mới", "example": "Edison was one of history's greatest inventors.", "ipa": "/ɪnˈventər/"},
                        {"word": "investor", "pos": "n.", "meaning": "Nhà đầu tư, người bỏ tiền vào kinh doanh", "example": "Investors funded the lightbulb project.", "ipa": "/ɪnˈvestər/"},
                        {"word": "patent", "pos": "n.", "meaning": "Bằng sáng chế, quyền đối với phát minh", "example": "Edison held patents for thousands of inventions.", "ipa": "/ˈpeɪtnt/"},
                        {"word": "ransack", "pos": "v.", "meaning": "Lục soát, tìm kiếm bừa bãi", "example": "Rivals ransacked his lab for secrets.", "ipa": "/ˈrænsæk/"},
                        {"word": "refinement", "pos": "n.", "meaning": "Sự cải tiến, hoàn thiện", "example": "The lightbulb required many refinements.", "ipa": "/rɪˈfaɪnmənt/"},
                        {"word": "ruling", "pos": "n.", "meaning": "Phán quyết pháp lý, quyết định của tòa", "example": "The court issued a ruling on the patent.", "ipa": "/ˈruːlɪŋ/"},
                        {"word": "specifically", "pos": "adv.", "meaning": "Cụ thể, đặc biệt vì lý do cụ thể", "example": "Edison specifically targeted commercial use.", "ipa": "/spəˈsɪfɪkli/"},
                        {"word": "suitable", "pos": "adj.", "meaning": "Phù hợp, thích hợp cho điều gì", "example": "Carbon proved suitable as a filament.", "ipa": "/ˈsuːtəbl/"},
                        {"word": "unveil", "pos": "v.", "meaning": "Tiết lộ, công bố ra công chúng", "example": "Edison unveiled the lightbulb in 1879.", "ipa": "/ˌʌnˈveɪl/"}
                    ]
                },
                {
                    "name": "Invention of Variable-Pitch Propellers",
                    "words": [
                        {"word": "aviation", "pos": "n.", "meaning": "Hàng không, việc phát triển và sử dụng máy bay", "example": "Aviation changed transportation forever.", "ipa": "/ˌeɪviˈeɪʃn/"},
                        {"word": "blade", "pos": "n.", "meaning": "Cánh mỏng của máy móc", "example": "Propeller blades can be adjusted in flight.", "ipa": "/bleɪd/"},
                        {"word": "coarse", "pos": "adj.", "meaning": "Thô ráp, không mịn", "example": "A coarse propeller works well at cruising speed.", "ipa": "/kɔːrs/"},
                        {"word": "confer", "pos": "v.", "meaning": "Thảo luận, tham khảo với ai đó", "example": "Engineers confer before testing new designs.", "ipa": "/kənˈfɜːr/"},
                        {"word": "cruise", "pos": "v.", "meaning": "Bay hoặc lái xe ở tốc độ ổn định", "example": "Planes cruise more efficiently at altitude.", "ipa": "/kruːz/"},
                        {"word": "curiosity", "pos": "n.", "meaning": "Sự tò mò, muốn biết điều mới", "example": "Curiosity drove Turnbull to experiment.", "ipa": "/ˌkjʊəriˈɒsəti/"},
                        {"word": "design", "pos": "n.", "meaning": "Thiết kế, bản vẽ kế hoạch", "example": "Turnbull's design was revolutionary.", "ipa": "/dɪˈzaɪn/"},
                        {"word": "enthusiast", "pos": "n.", "meaning": "Người đam mê nhiệt tình về điều gì", "example": "Turnbull was an aviation enthusiast.", "ipa": "/ɪnˈθjuːziæst/"},
                        {"word": "handle", "pos": "v.", "meaning": "Quản lý, vận hành tốt với", "example": "Variable-pitch propellers handle turbulence better.", "ipa": "/ˈhændl/"},
                        {"word": "inflexibility", "pos": "n.", "meaning": "Sự cứng nhắc, không có khả năng thay đổi", "example": "Fixed propellers suffered from inflexibility.", "ipa": "/ɪnˌfleksɪˈbɪləti/"},
                        {"word": "isolation", "pos": "n.", "meaning": "Sự cô lập, tình trạng bị tách biệt", "example": "Working in isolation slowed propeller development.", "ipa": "/ˌaɪsəˈleɪʃn/"},
                        {"word": "pitch", "pos": "n.", "meaning": "Góc nghiêng, độ dốc của cái gì đó", "example": "Changing the pitch improves efficiency.", "ipa": "/pɪtʃ/"},
                        {"word": "prolonged", "pos": "adj.", "meaning": "Kéo dài, thường theo nghĩa tiêu cực", "example": "Takeoffs were prolonged with old propellers.", "ipa": "/prəˈlɒŋd/"},
                        {"word": "propeller", "pos": "n.", "meaning": "Cánh quạt làm máy bay hoặc tàu di chuyển", "example": "The propeller design was patented in 1922.", "ipa": "/prəˈpelər/"},
                        {"word": "reliably", "pos": "adv.", "meaning": "Một cách đáng tin cậy", "example": "The new propeller worked reliably.", "ipa": "/rɪˈlaɪəbli/"},
                        {"word": "revolutionize", "pos": "v.", "meaning": "Thay đổi hoàn toàn, cách mạng hóa", "example": "The invention revolutionized air travel.", "ipa": "/ˌrevəˈluːʃənaɪz/"},
                        {"word": "rotation", "pos": "n.", "meaning": "Chuyển động quay tròn", "example": "Blade pitch changes with each rotation.", "ipa": "/roʊˈteɪʃn/"},
                        {"word": "sustained", "pos": "adj.", "meaning": "Duy trì được trong thời gian dài", "example": "Sustained flight requires efficient propellers.", "ipa": "/səˈsteɪnd/"},
                        {"word": "turbulence", "pos": "n.", "meaning": "Nhiễu loạn không khí, chuyển động mạnh đột ngột", "example": "Turbulence affects flight safety.", "ipa": "/ˈtɜːrbjələns/"},
                        {"word": "variable", "pos": "adj.", "meaning": "Có thể thay đổi, linh hoạt", "example": "Variable pitch gives pilots more control.", "ipa": "/ˈveəriəbl/"}
                    ]
                },
                {
                    "name": "The Transatlantic Cable",
                    "words": [
                        {"word": "cable", "pos": "n.", "meaning": "Cáp, dây điện dùng để truyền tín hiệu", "example": "The transatlantic cable connected continents.", "ipa": "/ˈkeɪbl/"},
                        {"word": "catastrophic", "pos": "adj.", "meaning": "Thảm khốc, cực kỳ tệ hại", "example": "The cable's failure was catastrophic.", "ipa": "/ˌkætəˈstrɒfɪk/"},
                        {"word": "compensate", "pos": "v.", "meaning": "Bù đắp, cân bằng", "example": "New technology compensated for earlier failures.", "ipa": "/ˈkɒmpenseɪt/"},
                        {"word": "disparate", "pos": "adj.", "meaning": "Khác biệt, không giống nhau", "example": "Disparate groups united to lay the cable.", "ipa": "/ˈdɪspərət/"},
                        {"word": "flaw", "pos": "n.", "meaning": "Sai sót, điểm yếu trong thiết kế", "example": "A flaw in insulation caused the cable to fail.", "ipa": "/flɔː/"},
                        {"word": "indispensable", "pos": "adj.", "meaning": "Không thể thiếu, hoàn toàn cần thiết", "example": "Fast communication became indispensable.", "ipa": "/ˌɪndɪˈspensəbl/"},
                        {"word": "inexplicably", "pos": "adv.", "meaning": "Không thể giải thích được, vô lý", "example": "The cable inexplicably stopped working.", "ipa": "/ɪnˈeksplɪkəbli/"},
                        {"word": "inquiry", "pos": "n.", "meaning": "Cuộc điều tra chính thức", "example": "A government inquiry investigated the failure.", "ipa": "/ɪnˈkwaɪəri/"},
                        {"word": "insulation", "pos": "n.", "meaning": "Vật liệu cách điện, nhiệt hoặc âm thanh", "example": "Good insulation is critical for undersea cables.", "ipa": "/ˌɪnsjəˈleɪʃn/"},
                        {"word": "perseverance", "pos": "n.", "meaning": "Sự kiên trì, tiếp tục dù có khó khăn", "example": "The cable's success required perseverance.", "ipa": "/ˌpɜːrsɪˈvɪərəns/"},
                        {"word": "rally", "pos": "v.", "meaning": "Tập hợp sự ủng hộ, đoàn kết lại", "example": "Field rallied investors to continue the project.", "ipa": "/ˈræli/"},
                        {"word": "requisite", "pos": "n.", "meaning": "Điều kiện cần thiết, yêu cầu", "example": "Funding was a requisite for the cable project.", "ipa": "/ˈrekwɪzɪt/"},
                        {"word": "set out", "pos": "v.", "meaning": "Bắt đầu một hoạt động, khởi hành", "example": "The team set out to lay the cable in 1857.", "ipa": "/set aʊt/"},
                        {"word": "snap", "pos": "v.", "meaning": "Đứt gãy đột ngột", "example": "The cable snapped during deployment.", "ipa": "/snæp/"},
                        {"word": "tow", "pos": "v.", "meaning": "Kéo theo sau", "example": "Ships towed the cable across the Atlantic.", "ipa": "/toʊ/"},
                        {"word": "transmit", "pos": "v.", "meaning": "Truyền tín hiệu, gửi đi", "example": "The cable transmitted messages across the ocean.", "ipa": "/trænsˈmɪt/"},
                        {"word": "triumph", "pos": "v.", "meaning": "Chiến thắng, thành công", "example": "They finally triumphed after many failures.", "ipa": "/ˈtraɪʌmf/"},
                        {"word": "utterly", "pos": "adv.", "meaning": "Hoàn toàn, tuyệt đối", "example": "The first attempt failed utterly.", "ipa": "/ˈʌtərli/"},
                        {"word": "vilified", "pos": "adj.", "meaning": "Bị bôi nhọ danh tiếng, bị nói xấu", "example": "The engineer was vilified for the failure.", "ipa": "/ˈvɪlɪfaɪd/"},
                        {"word": "voltage", "pos": "n.", "meaning": "Điện áp, đơn vị đo lực điện", "example": "High voltage damaged the early cable.", "ipa": "/ˈvoʊltɪdʒ/"}
                    ]
                }
            ]
        }
    ]
}

import json
print(json.dumps(vocab_data, ensure_ascii=False, indent=2)[:500])
print("...")
print(f"Total units: {len(vocab_data['units'])}")
total_words = sum(sum(len(t['words']) for t in u['topics']) for u in vocab_data['units'])
print(f"Total words: {total_words}")
PYEOF
python3 /tmp/build_vocab.py
