---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CognitiveServices.dll-Help.xml
Module Name: Az.CognitiveServices
ms.assetid: A2B4ACC1-6F53-47DE-A2D4-831E8AC89A5C
online version: https://docs.microsoft.com/en-us/powershell/module/az.cognitiveservices/new-azcognitiveservicesaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CognitiveServices/CognitiveServices/help/New-AzCognitiveServicesAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CognitiveServices/CognitiveServices/help/New-AzCognitiveServicesAccount.md
ms.openlocfilehash: 7e5253951ec3c74850584aaac9818a6a7c8f2737
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93710355"
---
# <span data-ttu-id="dd06a-101">New-AzCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="dd06a-101">New-AzCognitiveServicesAccount</span></span>

## <span data-ttu-id="dd06a-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="dd06a-102">SYNOPSIS</span></span>
<span data-ttu-id="dd06a-103">Tworzy konto usług poznawczych.</span><span class="sxs-lookup"><span data-stu-id="dd06a-103">Creates a Cognitive Services account.</span></span>

## <span data-ttu-id="dd06a-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="dd06a-104">SYNTAX</span></span>

```
New-AzCognitiveServicesAccount [-ResourceGroupName] <String> [-Name] <String> [-Type] <String>
 [-SkuName] <String> [-Location] <String> [-Tag <Hashtable[]>] [-CustomSubdomainName <String>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="dd06a-105">Opis</span><span class="sxs-lookup"><span data-stu-id="dd06a-105">DESCRIPTION</span></span>
<span data-ttu-id="dd06a-106">Polecenie cmdlet **New-AzCognitiveServicesAccount** umożliwia utworzenie konta usług poznawczych z określonym typem i magazynem SKU.</span><span class="sxs-lookup"><span data-stu-id="dd06a-106">The **New-AzCognitiveServicesAccount** cmdlet creates a Cognitive Services account with the specified type and SKU.</span></span>

## <span data-ttu-id="dd06a-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="dd06a-107">EXAMPLES</span></span>

### <span data-ttu-id="dd06a-108">1:1</span><span class="sxs-lookup"><span data-stu-id="dd06a-108">1:</span></span>
```
PS C:\> New-AzCognitiveServicesAccount -ResourceGroupName cognitive-services-resource-group -name myluis -Type LUIS -SkuName S0 -Locatio
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

## <span data-ttu-id="dd06a-109">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="dd06a-109">PARAMETERS</span></span>

### <span data-ttu-id="dd06a-110">-CustomSubdomainName</span><span class="sxs-lookup"><span data-stu-id="dd06a-110">-CustomSubdomainName</span></span>
<span data-ttu-id="dd06a-111">Nazwa poddomeny konta usług poznawczych.</span><span class="sxs-lookup"><span data-stu-id="dd06a-111">Cognitive Services Account Subdomain Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dd06a-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dd06a-112">-DefaultProfile</span></span>
<span data-ttu-id="dd06a-113">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="dd06a-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dd06a-114">-Force</span><span class="sxs-lookup"><span data-stu-id="dd06a-114">-Force</span></span>
<span data-ttu-id="dd06a-115">Wymusza uruchomienie polecenia bez monitowania o potwierdzenie użytkownika.</span><span class="sxs-lookup"><span data-stu-id="dd06a-115">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="dd06a-116">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="dd06a-116">-Location</span></span>
<span data-ttu-id="dd06a-117">Określa lokalizację, w której ma zostać utworzone konto.</span><span class="sxs-lookup"><span data-stu-id="dd06a-117">Specifies the location in which to create the account.</span></span>

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

### <span data-ttu-id="dd06a-118">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="dd06a-118">-Name</span></span>
<span data-ttu-id="dd06a-119">Określa nazwę konta.</span><span class="sxs-lookup"><span data-stu-id="dd06a-119">Specifies the name for the account.</span></span>

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

### <span data-ttu-id="dd06a-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dd06a-120">-ResourceGroupName</span></span>
<span data-ttu-id="dd06a-121">Określa nazwę grupy zasobów, do której ma zostać przypisane konto.</span><span class="sxs-lookup"><span data-stu-id="dd06a-121">Specifies the name of the resource group to which to assign the account.</span></span>
<span data-ttu-id="dd06a-122">Grupa zasobów musi już istnieć.</span><span class="sxs-lookup"><span data-stu-id="dd06a-122">The resource group must already exist.</span></span>

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

### <span data-ttu-id="dd06a-123">-SkuName</span><span class="sxs-lookup"><span data-stu-id="dd06a-123">-SkuName</span></span>
<span data-ttu-id="dd06a-124">Określa jednostkę SKU konta.</span><span class="sxs-lookup"><span data-stu-id="dd06a-124">Specifies the SKU for the account.</span></span>
<span data-ttu-id="dd06a-125">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="dd06a-125">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="dd06a-126">F0 (warstwa wolna)</span><span class="sxs-lookup"><span data-stu-id="dd06a-126">F0 (free tier)</span></span>
- <span data-ttu-id="dd06a-127">S0</span><span class="sxs-lookup"><span data-stu-id="dd06a-127">S0</span></span>
- <span data-ttu-id="dd06a-128">S1</span><span class="sxs-lookup"><span data-stu-id="dd06a-128">S1</span></span>
- <span data-ttu-id="dd06a-129">S2</span><span class="sxs-lookup"><span data-stu-id="dd06a-129">S2</span></span>
- <span data-ttu-id="dd06a-130">S3</span><span class="sxs-lookup"><span data-stu-id="dd06a-130">S3</span></span>
- <span data-ttu-id="dd06a-131">S4 Aby uzyskać więcej informacji, zobacz [interfejsy API usług poznawczych](https://www.microsoft.com/cognitive-services/en-us/apis).</span><span class="sxs-lookup"><span data-stu-id="dd06a-131">S4 For more information, see [Cognitive Service APIs](https://www.microsoft.com/cognitive-services/en-us/apis).</span></span>

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

### <span data-ttu-id="dd06a-132">-Tag</span><span class="sxs-lookup"><span data-stu-id="dd06a-132">-Tag</span></span>
<span data-ttu-id="dd06a-133">Określa tag jako parę nazwa/wartość.</span><span class="sxs-lookup"><span data-stu-id="dd06a-133">Specifies a tag as a name/value pair.</span></span>

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

### <span data-ttu-id="dd06a-134">-Type</span><span class="sxs-lookup"><span data-stu-id="dd06a-134">-Type</span></span>
<span data-ttu-id="dd06a-135">Określa typ konta, które ma zostać utworzone.</span><span class="sxs-lookup"><span data-stu-id="dd06a-135">Specifies the type of account to create.</span></span> <span data-ttu-id="dd06a-136">Użyj `Get-AzCognitiveServicesAccountType` polecenia cmdlet, aby uzyskać bieżące dopuszczalne wartości.</span><span class="sxs-lookup"><span data-stu-id="dd06a-136">Use `Get-AzCognitiveServicesAccountType` cmdlet to get current acceptable values.</span></span>

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

### <span data-ttu-id="dd06a-137">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="dd06a-137">-Confirm</span></span>
<span data-ttu-id="dd06a-138">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="dd06a-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="dd06a-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dd06a-139">-WhatIf</span></span>
<span data-ttu-id="dd06a-140">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="dd06a-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="dd06a-141">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="dd06a-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="dd06a-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dd06a-142">CommonParameters</span></span>
<span data-ttu-id="dd06a-143">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dd06a-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dd06a-144">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dd06a-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dd06a-145">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="dd06a-145">INPUTS</span></span>

### <span data-ttu-id="dd06a-146">System. String</span><span class="sxs-lookup"><span data-stu-id="dd06a-146">System.String</span></span>

## <span data-ttu-id="dd06a-147">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="dd06a-147">OUTPUTS</span></span>

### <span data-ttu-id="dd06a-148">Microsoft. Azure. Commands. Management. CognitiveServices. models. PSCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="dd06a-148">Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSCognitiveServicesAccount</span></span>

## <span data-ttu-id="dd06a-149">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="dd06a-149">NOTES</span></span>

## <span data-ttu-id="dd06a-150">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="dd06a-150">RELATED LINKS</span></span>

[<span data-ttu-id="dd06a-151">Get-AzCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="dd06a-151">Get-AzCognitiveServicesAccount</span></span>](./Get-AzCognitiveServicesAccount.md)

[<span data-ttu-id="dd06a-152">Remove-AzCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="dd06a-152">Remove-AzCognitiveServicesAccount</span></span>](./Remove-AzCognitiveServicesAccount.md)

[<span data-ttu-id="dd06a-153">Set-AzCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="dd06a-153">Set-AzCognitiveServicesAccount</span></span>](./Set-AzCognitiveServicesAccount.md)
