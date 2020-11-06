---
external help file: Microsoft.Azure.Commands.Management.CognitiveServices.dll-Help.xml
Module Name: AzureRM.CognitiveServices
ms.assetid: A2B4ACC1-6F53-47DE-A2D4-831E8AC89A5C
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.cognitiveservices/new-azurermcognitiveservicesaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/CognitiveServices/Commands.Management.CognitiveServices/help/New-AzureRmCognitiveServicesAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/CognitiveServices/Commands.Management.CognitiveServices/help/New-AzureRmCognitiveServicesAccount.md
ms.openlocfilehash: 41defe467244647f707bae16c653dfcbe99eaec3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93543924"
---
# <span data-ttu-id="29dcd-101">New-AzureRmCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="29dcd-101">New-AzureRmCognitiveServicesAccount</span></span>

## <span data-ttu-id="29dcd-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="29dcd-102">SYNOPSIS</span></span>
<span data-ttu-id="29dcd-103">Tworzy konto usług poznawczych.</span><span class="sxs-lookup"><span data-stu-id="29dcd-103">Creates a Cognitive Services account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="29dcd-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="29dcd-104">SYNTAX</span></span>

```
New-AzureRmCognitiveServicesAccount [-ResourceGroupName] <String> [-Name] <String> [-Type] <String>
 [-SkuName] <String> [-Location] <String> [-Tag <Hashtable[]>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="29dcd-105">Opis</span><span class="sxs-lookup"><span data-stu-id="29dcd-105">DESCRIPTION</span></span>
<span data-ttu-id="29dcd-106">Polecenie cmdlet **New-AzureRmCognitiveServicesAccount** umożliwia utworzenie konta usług poznawczych z określonym typem i magazynem SKU.</span><span class="sxs-lookup"><span data-stu-id="29dcd-106">The **New-AzureRmCognitiveServicesAccount** cmdlet creates a Cognitive Services account with the specified type and SKU.</span></span>

## <span data-ttu-id="29dcd-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="29dcd-107">EXAMPLES</span></span>

### <span data-ttu-id="29dcd-108">1:1</span><span class="sxs-lookup"><span data-stu-id="29dcd-108">1:</span></span>
```
PS C:\> New-AzureRmCognitiveServicesAccount -ResourceGroupName cognitive-services-resource-group -name myluis -Type LUIS -SkuName S0 -Locatio
n 'WestUS'


ResourceGroupName : cognitive-services-resource-group
AccountName       : myluis
Id                : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/cognitive-services-resource-group/providers/Microsoft.Cog
                    nitiveServices/accounts/myluis
Endpoint          : https://westus.api.cognitive.microsoft.com/luis/v2.0
Location          : WestUS
Sku               : Microsoft.Azure.Management.CognitiveServices.Models.Sku
AccountType       : LUIS
ResourceType      : Microsoft.CognitiveServices/accounts
Etag              : "xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx"
ProvisioningState : Succeeded
Tags              :
```

## <span data-ttu-id="29dcd-109">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="29dcd-109">PARAMETERS</span></span>

### <span data-ttu-id="29dcd-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="29dcd-110">-DefaultProfile</span></span>
<span data-ttu-id="29dcd-111">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="29dcd-111">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="29dcd-112">-Force</span><span class="sxs-lookup"><span data-stu-id="29dcd-112">-Force</span></span>
<span data-ttu-id="29dcd-113">Wymusza uruchomienie polecenia bez monitowania o potwierdzenie użytkownika.</span><span class="sxs-lookup"><span data-stu-id="29dcd-113">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="29dcd-114">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="29dcd-114">-Location</span></span>
<span data-ttu-id="29dcd-115">Określa lokalizację, w której ma zostać utworzone konto.</span><span class="sxs-lookup"><span data-stu-id="29dcd-115">Specifies the location in which to create the account.</span></span>

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

### <span data-ttu-id="29dcd-116">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="29dcd-116">-Name</span></span>
<span data-ttu-id="29dcd-117">Określa nazwę konta.</span><span class="sxs-lookup"><span data-stu-id="29dcd-117">Specifies the name for the account.</span></span>

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

### <span data-ttu-id="29dcd-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="29dcd-118">-ResourceGroupName</span></span>
<span data-ttu-id="29dcd-119">Określa nazwę grupy zasobów, do której ma zostać przypisane konto.</span><span class="sxs-lookup"><span data-stu-id="29dcd-119">Specifies the name of the resource group to which to assign the account.</span></span>
<span data-ttu-id="29dcd-120">Grupa zasobów musi już istnieć.</span><span class="sxs-lookup"><span data-stu-id="29dcd-120">The resource group must already exist.</span></span>

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

### <span data-ttu-id="29dcd-121">-SkuName</span><span class="sxs-lookup"><span data-stu-id="29dcd-121">-SkuName</span></span>
<span data-ttu-id="29dcd-122">Określa jednostkę SKU konta.</span><span class="sxs-lookup"><span data-stu-id="29dcd-122">Specifies the SKU for the account.</span></span>
<span data-ttu-id="29dcd-123">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="29dcd-123">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="29dcd-124">F0 (warstwa wolna)</span><span class="sxs-lookup"><span data-stu-id="29dcd-124">F0 (free tier)</span></span>
- <span data-ttu-id="29dcd-125">S0</span><span class="sxs-lookup"><span data-stu-id="29dcd-125">S0</span></span>
- <span data-ttu-id="29dcd-126">S1</span><span class="sxs-lookup"><span data-stu-id="29dcd-126">S1</span></span>
- <span data-ttu-id="29dcd-127">S2</span><span class="sxs-lookup"><span data-stu-id="29dcd-127">S2</span></span>
- <span data-ttu-id="29dcd-128">S3</span><span class="sxs-lookup"><span data-stu-id="29dcd-128">S3</span></span>
- <span data-ttu-id="29dcd-129">S4 Aby uzyskać więcej informacji, zobacz [interfejsy API usług poznawczych](https://www.microsoft.com/cognitive-services/en-us/apis).</span><span class="sxs-lookup"><span data-stu-id="29dcd-129">S4 For more information, see [Cognitive Service APIs](https://www.microsoft.com/cognitive-services/en-us/apis).</span></span>

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

### <span data-ttu-id="29dcd-130">-Tag</span><span class="sxs-lookup"><span data-stu-id="29dcd-130">-Tag</span></span>
<span data-ttu-id="29dcd-131">Określa tag jako parę nazwa/wartość.</span><span class="sxs-lookup"><span data-stu-id="29dcd-131">Specifies a tag as a name/value pair.</span></span>

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

### <span data-ttu-id="29dcd-132">-Type</span><span class="sxs-lookup"><span data-stu-id="29dcd-132">-Type</span></span>
<span data-ttu-id="29dcd-133">Określa typ konta, które ma zostać utworzone.</span><span class="sxs-lookup"><span data-stu-id="29dcd-133">Specifies the type of account to create.</span></span> <span data-ttu-id="29dcd-134">Użyj `Get-AzureRmCognitiveServicesAccountType` polecenia cmdlet, aby uzyskać bieżące dopuszczalne wartości.</span><span class="sxs-lookup"><span data-stu-id="29dcd-134">Use `Get-AzureRmCognitiveServicesAccountType` cmdlet to get current acceptable values.</span></span>

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

### <span data-ttu-id="29dcd-135">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="29dcd-135">-Confirm</span></span>
<span data-ttu-id="29dcd-136">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="29dcd-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="29dcd-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="29dcd-137">-WhatIf</span></span>
<span data-ttu-id="29dcd-138">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="29dcd-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="29dcd-139">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="29dcd-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="29dcd-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="29dcd-140">CommonParameters</span></span>
<span data-ttu-id="29dcd-141">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="29dcd-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="29dcd-142">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="29dcd-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="29dcd-143">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="29dcd-143">INPUTS</span></span>

### <span data-ttu-id="29dcd-144">System. String</span><span class="sxs-lookup"><span data-stu-id="29dcd-144">System.String</span></span>

## <span data-ttu-id="29dcd-145">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="29dcd-145">OUTPUTS</span></span>

### <span data-ttu-id="29dcd-146">Microsoft. Azure. Commands. Management. CognitiveServices. models. PSCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="29dcd-146">Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSCognitiveServicesAccount</span></span>

## <span data-ttu-id="29dcd-147">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="29dcd-147">NOTES</span></span>

## <span data-ttu-id="29dcd-148">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="29dcd-148">RELATED LINKS</span></span>

[<span data-ttu-id="29dcd-149">Get-AzureRmCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="29dcd-149">Get-AzureRmCognitiveServicesAccount</span></span>](./Get-AzureRmCognitiveServicesAccount.md)

[<span data-ttu-id="29dcd-150">Remove-AzureRmCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="29dcd-150">Remove-AzureRmCognitiveServicesAccount</span></span>](./Remove-AzureRmCognitiveServicesAccount.md)

[<span data-ttu-id="29dcd-151">Set-AzureRmCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="29dcd-151">Set-AzureRmCognitiveServicesAccount</span></span>](./Set-AzureRmCognitiveServicesAccount.md)
