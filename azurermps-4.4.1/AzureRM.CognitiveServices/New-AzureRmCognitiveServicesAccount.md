---
external help file: Microsoft.Azure.Commands.Management.CognitiveServices.dll-Help.xml
Module Name: AzureRM.CognitiveServices
ms.assetid: A2B4ACC1-6F53-47DE-A2D4-831E8AC89A5C
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/CognitiveServices/Commands.Management.CognitiveServices/help/New-AzureRmCognitiveServicesAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/CognitiveServices/Commands.Management.CognitiveServices/help/New-AzureRmCognitiveServicesAccount.md
ms.openlocfilehash: 449b10f851dbd4e2f2e804bab0772543d512c0c0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93554012"
---
# <span data-ttu-id="3fe0a-101">New-AzureRmCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="3fe0a-101">New-AzureRmCognitiveServicesAccount</span></span>

## <span data-ttu-id="3fe0a-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="3fe0a-102">SYNOPSIS</span></span>
<span data-ttu-id="3fe0a-103">Tworzy konto usług poznawczych.</span><span class="sxs-lookup"><span data-stu-id="3fe0a-103">Creates a Cognitive Services account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3fe0a-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="3fe0a-104">SYNTAX</span></span>

```
New-AzureRmCognitiveServicesAccount [-ResourceGroupName] <String> [-Name] <String> [-Type] <String>
 [-SkuName] <String> [-Location] <String> [-Tag <Hashtable[]>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3fe0a-105">Opis</span><span class="sxs-lookup"><span data-stu-id="3fe0a-105">DESCRIPTION</span></span>
<span data-ttu-id="3fe0a-106">Polecenie cmdlet **New-AzureRmCognitiveServicesAccount** umożliwia utworzenie konta usług poznawczych z określonym typem i magazynem SKU.</span><span class="sxs-lookup"><span data-stu-id="3fe0a-106">The **New-AzureRmCognitiveServicesAccount** cmdlet creates a Cognitive Services account with the specified type and SKU.</span></span>

## <span data-ttu-id="3fe0a-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="3fe0a-107">EXAMPLES</span></span>

### <span data-ttu-id="3fe0a-108">1:1</span><span class="sxs-lookup"><span data-stu-id="3fe0a-108">1:</span></span>
```
New-AzureRmCognitiveServicesAccount -ResourceGroupName 'resourcegroup1' -name 'MyAccountName' -Type TextTranslation -SkuName F0 -Location 'usgovvirginia'
```

## <span data-ttu-id="3fe0a-109">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="3fe0a-109">PARAMETERS</span></span>

### <span data-ttu-id="3fe0a-110">-Force</span><span class="sxs-lookup"><span data-stu-id="3fe0a-110">-Force</span></span>
<span data-ttu-id="3fe0a-111">Wymusza uruchomienie polecenia bez monitowania o potwierdzenie użytkownika.</span><span class="sxs-lookup"><span data-stu-id="3fe0a-111">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3fe0a-112">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="3fe0a-112">-Location</span></span>
<span data-ttu-id="3fe0a-113">Określa lokalizację, w której ma zostać utworzone konto.</span><span class="sxs-lookup"><span data-stu-id="3fe0a-113">Specifies the location in which to create the account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3fe0a-114">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="3fe0a-114">-Name</span></span>
<span data-ttu-id="3fe0a-115">Określa nazwę konta.</span><span class="sxs-lookup"><span data-stu-id="3fe0a-115">Specifies the name for the account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: CognitiveServicesAccountName, AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3fe0a-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3fe0a-116">-ResourceGroupName</span></span>
<span data-ttu-id="3fe0a-117">Określa nazwę grupy zasobów, do której ma zostać przypisane konto.</span><span class="sxs-lookup"><span data-stu-id="3fe0a-117">Specifies the name of the resource group to which to assign the account.</span></span>
<span data-ttu-id="3fe0a-118">Grupa zasobów musi już istnieć.</span><span class="sxs-lookup"><span data-stu-id="3fe0a-118">The resource group must already exist.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3fe0a-119">-SkuName</span><span class="sxs-lookup"><span data-stu-id="3fe0a-119">-SkuName</span></span>
<span data-ttu-id="3fe0a-120">Określa jednostkę SKU konta.</span><span class="sxs-lookup"><span data-stu-id="3fe0a-120">Specifies the SKU for the account.</span></span>
<span data-ttu-id="3fe0a-121">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="3fe0a-121">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="3fe0a-122">F0 (warstwa wolna)</span><span class="sxs-lookup"><span data-stu-id="3fe0a-122">F0 (free tier)</span></span>
- <span data-ttu-id="3fe0a-123">S0</span><span class="sxs-lookup"><span data-stu-id="3fe0a-123">S0</span></span>
- <span data-ttu-id="3fe0a-124">S1</span><span class="sxs-lookup"><span data-stu-id="3fe0a-124">S1</span></span>
- <span data-ttu-id="3fe0a-125">S2</span><span class="sxs-lookup"><span data-stu-id="3fe0a-125">S2</span></span>
- <span data-ttu-id="3fe0a-126">S3</span><span class="sxs-lookup"><span data-stu-id="3fe0a-126">S3</span></span>
- <span data-ttu-id="3fe0a-127">Stanu</span><span class="sxs-lookup"><span data-stu-id="3fe0a-127">S4</span></span>

<span data-ttu-id="3fe0a-128">Aby uzyskać więcej informacji, zobacz [interfejsy API usług poznawczych](https://www.microsoft.com/cognitive-services/en-us/apis).</span><span class="sxs-lookup"><span data-stu-id="3fe0a-128">For more information, see [Cognitive Service APIs](https://www.microsoft.com/cognitive-services/en-us/apis).</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3fe0a-129">-Tag</span><span class="sxs-lookup"><span data-stu-id="3fe0a-129">-Tag</span></span>
<span data-ttu-id="3fe0a-130">Określa tag jako parę nazwa/wartość.</span><span class="sxs-lookup"><span data-stu-id="3fe0a-130">Specifies a tag as a name/value pair.</span></span>

```yaml
Type: System.Collections.Hashtable[]
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3fe0a-131">-Type</span><span class="sxs-lookup"><span data-stu-id="3fe0a-131">-Type</span></span>
<span data-ttu-id="3fe0a-132">Określa typ konta, które ma zostać utworzone. Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="3fe0a-132">Specifies the type of account to create.The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="3fe0a-133">ComputerVision</span><span class="sxs-lookup"><span data-stu-id="3fe0a-133">ComputerVision</span></span>
- <span data-ttu-id="3fe0a-134">Emocji</span><span class="sxs-lookup"><span data-stu-id="3fe0a-134">Emotion</span></span>
- <span data-ttu-id="3fe0a-135">Silne</span><span class="sxs-lookup"><span data-stu-id="3fe0a-135">Face</span></span>
- <span data-ttu-id="3fe0a-136">LUIS</span><span class="sxs-lookup"><span data-stu-id="3fe0a-136">LUIS</span></span>
- <span data-ttu-id="3fe0a-137">Przygotowanie</span><span class="sxs-lookup"><span data-stu-id="3fe0a-137">Recommendations</span></span>
- <span data-ttu-id="3fe0a-138">Postaci</span><span class="sxs-lookup"><span data-stu-id="3fe0a-138">Speech</span></span>
- <span data-ttu-id="3fe0a-139">Analiza autoanalizy</span><span class="sxs-lookup"><span data-stu-id="3fe0a-139">TextAnalytics</span></span>
- <span data-ttu-id="3fe0a-140">WebLM</span><span class="sxs-lookup"><span data-stu-id="3fe0a-140">WebLM</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: CognitiveServicesAccountType, AccountType, Kind

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3fe0a-141">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="3fe0a-141">-Confirm</span></span>
<span data-ttu-id="3fe0a-142">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3fe0a-142">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3fe0a-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3fe0a-143">-WhatIf</span></span>
<span data-ttu-id="3fe0a-144">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3fe0a-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3fe0a-145">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="3fe0a-145">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3fe0a-146">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3fe0a-146">-DefaultProfile</span></span>
<span data-ttu-id="3fe0a-147">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="3fe0a-147">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3fe0a-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3fe0a-148">CommonParameters</span></span>
<span data-ttu-id="3fe0a-149">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3fe0a-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3fe0a-150">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3fe0a-150">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3fe0a-151">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="3fe0a-151">INPUTS</span></span>

## <span data-ttu-id="3fe0a-152">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="3fe0a-152">OUTPUTS</span></span>

### <span data-ttu-id="3fe0a-153">Microsoft. Azure. Commands. Management. CognitiveServices. models. PSCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="3fe0a-153">Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSCognitiveServicesAccount</span></span>

## <span data-ttu-id="3fe0a-154">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="3fe0a-154">NOTES</span></span>

## <span data-ttu-id="3fe0a-155">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="3fe0a-155">RELATED LINKS</span></span>

[<span data-ttu-id="3fe0a-156">Get-AzureRmCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="3fe0a-156">Get-AzureRmCognitiveServicesAccount</span></span>](./Get-AzureRmCognitiveServicesAccount.md)

[<span data-ttu-id="3fe0a-157">Remove-AzureRmCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="3fe0a-157">Remove-AzureRmCognitiveServicesAccount</span></span>](./Remove-AzureRmCognitiveServicesAccount.md)

[<span data-ttu-id="3fe0a-158">Set-AzureRmCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="3fe0a-158">Set-AzureRmCognitiveServicesAccount</span></span>](./Set-AzureRmCognitiveServicesAccount.md)
