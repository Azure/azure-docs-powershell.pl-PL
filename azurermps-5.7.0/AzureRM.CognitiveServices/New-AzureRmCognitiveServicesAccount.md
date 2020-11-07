---
external help file: Microsoft.Azure.Commands.Management.CognitiveServices.dll-Help.xml
Module Name: AzureRM.CognitiveServices
ms.assetid: A2B4ACC1-6F53-47DE-A2D4-831E8AC89A5C
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.cognitiveservices/new-azurermcognitiveservicesaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/CognitiveServices/Commands.Management.CognitiveServices/help/New-AzureRmCognitiveServicesAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/CognitiveServices/Commands.Management.CognitiveServices/help/New-AzureRmCognitiveServicesAccount.md
ms.openlocfilehash: 1c1d4ad776ed3db2cb3b5adfb490902a7de12f42
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93716638"
---
# <span data-ttu-id="6823e-101">New-AzureRmCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="6823e-101">New-AzureRmCognitiveServicesAccount</span></span>

## <span data-ttu-id="6823e-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="6823e-102">SYNOPSIS</span></span>
<span data-ttu-id="6823e-103">Tworzy konto usług poznawczych.</span><span class="sxs-lookup"><span data-stu-id="6823e-103">Creates a Cognitive Services account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6823e-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="6823e-104">SYNTAX</span></span>

```
New-AzureRmCognitiveServicesAccount [-ResourceGroupName] <String> [-Name] <String> [-Type] <String>
 [-SkuName] <String> [-Location] <String> [-Tag <Hashtable[]>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6823e-105">Opis</span><span class="sxs-lookup"><span data-stu-id="6823e-105">DESCRIPTION</span></span>
<span data-ttu-id="6823e-106">Polecenie cmdlet **New-AzureRmCognitiveServicesAccount** umożliwia utworzenie konta usług poznawczych z określonym typem i magazynem SKU.</span><span class="sxs-lookup"><span data-stu-id="6823e-106">The **New-AzureRmCognitiveServicesAccount** cmdlet creates a Cognitive Services account with the specified type and SKU.</span></span>

## <span data-ttu-id="6823e-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="6823e-107">EXAMPLES</span></span>

### <span data-ttu-id="6823e-108">1:1</span><span class="sxs-lookup"><span data-stu-id="6823e-108">1:</span></span>
```
New-AzureRmCognitiveServicesAccount -ResourceGroupName 'resourcegroup1' -name 'MyAccountName' -Type TextTranslation -SkuName F0 -Location 'usgovvirginia'
```

## <span data-ttu-id="6823e-109">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="6823e-109">PARAMETERS</span></span>

### <span data-ttu-id="6823e-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6823e-110">-DefaultProfile</span></span>
<span data-ttu-id="6823e-111">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="6823e-111">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6823e-112">-Force</span><span class="sxs-lookup"><span data-stu-id="6823e-112">-Force</span></span>
<span data-ttu-id="6823e-113">Wymusza uruchomienie polecenia bez monitowania o potwierdzenie użytkownika.</span><span class="sxs-lookup"><span data-stu-id="6823e-113">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6823e-114">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="6823e-114">-Location</span></span>
<span data-ttu-id="6823e-115">Określa lokalizację, w której ma zostać utworzone konto.</span><span class="sxs-lookup"><span data-stu-id="6823e-115">Specifies the location in which to create the account.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6823e-116">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="6823e-116">-Name</span></span>
<span data-ttu-id="6823e-117">Określa nazwę konta.</span><span class="sxs-lookup"><span data-stu-id="6823e-117">Specifies the name for the account.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: CognitiveServicesAccountName, AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6823e-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6823e-118">-ResourceGroupName</span></span>
<span data-ttu-id="6823e-119">Określa nazwę grupy zasobów, do której ma zostać przypisane konto.</span><span class="sxs-lookup"><span data-stu-id="6823e-119">Specifies the name of the resource group to which to assign the account.</span></span>
<span data-ttu-id="6823e-120">Grupa zasobów musi już istnieć.</span><span class="sxs-lookup"><span data-stu-id="6823e-120">The resource group must already exist.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6823e-121">-SkuName</span><span class="sxs-lookup"><span data-stu-id="6823e-121">-SkuName</span></span>
<span data-ttu-id="6823e-122">Określa jednostkę SKU konta.</span><span class="sxs-lookup"><span data-stu-id="6823e-122">Specifies the SKU for the account.</span></span>
<span data-ttu-id="6823e-123">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="6823e-123">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="6823e-124">F0 (warstwa wolna)</span><span class="sxs-lookup"><span data-stu-id="6823e-124">F0 (free tier)</span></span>
- <span data-ttu-id="6823e-125">S0</span><span class="sxs-lookup"><span data-stu-id="6823e-125">S0</span></span>
- <span data-ttu-id="6823e-126">S1</span><span class="sxs-lookup"><span data-stu-id="6823e-126">S1</span></span>
- <span data-ttu-id="6823e-127">S2</span><span class="sxs-lookup"><span data-stu-id="6823e-127">S2</span></span>
- <span data-ttu-id="6823e-128">S3</span><span class="sxs-lookup"><span data-stu-id="6823e-128">S3</span></span>
- <span data-ttu-id="6823e-129">Stanu</span><span class="sxs-lookup"><span data-stu-id="6823e-129">S4</span></span>

<span data-ttu-id="6823e-130">Aby uzyskać więcej informacji, zobacz [interfejsy API usług poznawczych](https://www.microsoft.com/cognitive-services/en-us/apis).</span><span class="sxs-lookup"><span data-stu-id="6823e-130">For more information, see [Cognitive Service APIs](https://www.microsoft.com/cognitive-services/en-us/apis).</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6823e-131">-Tag</span><span class="sxs-lookup"><span data-stu-id="6823e-131">-Tag</span></span>
<span data-ttu-id="6823e-132">Określa tag jako parę nazwa/wartość.</span><span class="sxs-lookup"><span data-stu-id="6823e-132">Specifies a tag as a name/value pair.</span></span>

```yaml
Type: Hashtable[]
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6823e-133">-Type</span><span class="sxs-lookup"><span data-stu-id="6823e-133">-Type</span></span>
<span data-ttu-id="6823e-134">Określa typ konta, które ma zostać utworzone.</span><span class="sxs-lookup"><span data-stu-id="6823e-134">Specifies the type of account to create.</span></span> <span data-ttu-id="6823e-135">Bieżące dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="6823e-135">Current acceptable values for this parameter are:</span></span>

- <span data-ttu-id="6823e-136">Usługa Bing. autosugerował. v7</span><span class="sxs-lookup"><span data-stu-id="6823e-136">Bing.Autosuggest.v7</span></span>
- <span data-ttu-id="6823e-137">Bing. CustomSearch</span><span class="sxs-lookup"><span data-stu-id="6823e-137">Bing.CustomSearch</span></span>
- <span data-ttu-id="6823e-138">Usługa Bing. Search. v7</span><span class="sxs-lookup"><span data-stu-id="6823e-138">Bing.Search.v7</span></span>
- <span data-ttu-id="6823e-139">Bing. mowa</span><span class="sxs-lookup"><span data-stu-id="6823e-139">Bing.Speech</span></span>
- <span data-ttu-id="6823e-140">Bing. Sprawdzanie pisowni. v7</span><span class="sxs-lookup"><span data-stu-id="6823e-140">Bing.SpellCheck.v7</span></span>
- <span data-ttu-id="6823e-141">ComputerVision</span><span class="sxs-lookup"><span data-stu-id="6823e-141">ComputerVision</span></span>
- <span data-ttu-id="6823e-142">ContentModerator</span><span class="sxs-lookup"><span data-stu-id="6823e-142">ContentModerator</span></span>
- <span data-ttu-id="6823e-143">CustomSpeech</span><span class="sxs-lookup"><span data-stu-id="6823e-143">CustomSpeech</span></span>
- <span data-ttu-id="6823e-144">CustomVision. przewidywania</span><span class="sxs-lookup"><span data-stu-id="6823e-144">CustomVision.Prediction</span></span>
- <span data-ttu-id="6823e-145">CustomVision. szkolenia</span><span class="sxs-lookup"><span data-stu-id="6823e-145">CustomVision.Training</span></span>
- <span data-ttu-id="6823e-146">Emocji</span><span class="sxs-lookup"><span data-stu-id="6823e-146">Emotion</span></span>
- <span data-ttu-id="6823e-147">Silne</span><span class="sxs-lookup"><span data-stu-id="6823e-147">Face</span></span>
- <span data-ttu-id="6823e-148">LUIS</span><span class="sxs-lookup"><span data-stu-id="6823e-148">LUIS</span></span>
- <span data-ttu-id="6823e-149">QnAMaker</span><span class="sxs-lookup"><span data-stu-id="6823e-149">QnAMaker</span></span>
- <span data-ttu-id="6823e-150">SpeakerRecognition</span><span class="sxs-lookup"><span data-stu-id="6823e-150">SpeakerRecognition</span></span>
- <span data-ttu-id="6823e-151">SpeechTranslation</span><span class="sxs-lookup"><span data-stu-id="6823e-151">SpeechTranslation</span></span>
- <span data-ttu-id="6823e-152">Analiza autoanalizy</span><span class="sxs-lookup"><span data-stu-id="6823e-152">TextAnalytics</span></span>
- <span data-ttu-id="6823e-153">Tłumaczenie</span><span class="sxs-lookup"><span data-stu-id="6823e-153">TextTranslation</span></span>
- <span data-ttu-id="6823e-154">WebLM</span><span class="sxs-lookup"><span data-stu-id="6823e-154">WebLM</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: CognitiveServicesAccountType, AccountType, Kind

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6823e-155">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="6823e-155">-Confirm</span></span>
<span data-ttu-id="6823e-156">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6823e-156">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6823e-157">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6823e-157">-WhatIf</span></span>
<span data-ttu-id="6823e-158">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6823e-158">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6823e-159">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="6823e-159">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6823e-160">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6823e-160">CommonParameters</span></span>
<span data-ttu-id="6823e-161">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6823e-161">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6823e-162">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6823e-162">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6823e-163">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="6823e-163">INPUTS</span></span>

### <span data-ttu-id="6823e-164">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="6823e-164">None</span></span>
<span data-ttu-id="6823e-165">To polecenie cmdlet nie akceptuje żadnych danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="6823e-165">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="6823e-166">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="6823e-166">OUTPUTS</span></span>

### <span data-ttu-id="6823e-167">Microsoft. Azure. Commands. Management. CognitiveServices. models. PSCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="6823e-167">Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSCognitiveServicesAccount</span></span>

## <span data-ttu-id="6823e-168">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="6823e-168">NOTES</span></span>

## <span data-ttu-id="6823e-169">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="6823e-169">RELATED LINKS</span></span>

[<span data-ttu-id="6823e-170">Get-AzureRmCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="6823e-170">Get-AzureRmCognitiveServicesAccount</span></span>](./Get-AzureRmCognitiveServicesAccount.md)

[<span data-ttu-id="6823e-171">Remove-AzureRmCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="6823e-171">Remove-AzureRmCognitiveServicesAccount</span></span>](./Remove-AzureRmCognitiveServicesAccount.md)

[<span data-ttu-id="6823e-172">Set-AzureRmCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="6823e-172">Set-AzureRmCognitiveServicesAccount</span></span>](./Set-AzureRmCognitiveServicesAccount.md)
