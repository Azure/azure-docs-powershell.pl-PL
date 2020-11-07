---
external help file: Microsoft.Azure.Commands.Management.CognitiveServices.dll-Help.xml
Module Name: AzureRM.CognitiveServices
ms.assetid: 11E2D82A-1DF1-4E19-8328-44674641D1BB
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.cognitiveservices/set-azurermcognitiveservicesaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/CognitiveServices/Commands.Management.CognitiveServices/help/Set-AzureRmCognitiveServicesAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/CognitiveServices/Commands.Management.CognitiveServices/help/Set-AzureRmCognitiveServicesAccount.md
ms.openlocfilehash: 74c066cd59497603da4f953f35ed16e454e67155
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93717272"
---
# <span data-ttu-id="87139-101">Set-AzureRmCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="87139-101">Set-AzureRmCognitiveServicesAccount</span></span>

## <span data-ttu-id="87139-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="87139-102">SYNOPSIS</span></span>
<span data-ttu-id="87139-103">Modyfikuje konto.</span><span class="sxs-lookup"><span data-stu-id="87139-103">Modifies an account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="87139-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="87139-104">SYNTAX</span></span>

```
Set-AzureRmCognitiveServicesAccount [-ResourceGroupName] <String> [-Name] <String> [-SkuName <String>]
 [-Tag <Hashtable[]>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="87139-105">Opis</span><span class="sxs-lookup"><span data-stu-id="87139-105">DESCRIPTION</span></span>
<span data-ttu-id="87139-106">Polecenie cmdlet **Set-AzureRmCognitiveServicesAccount** modyfikuje jednostkę SKU lub Tagi określonego konta usług poznawczych.</span><span class="sxs-lookup"><span data-stu-id="87139-106">The **Set-AzureRmCognitiveServicesAccount** cmdlet modifies the SKU or tags of the specified Cognitive Services account.</span></span>

## <span data-ttu-id="87139-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="87139-107">EXAMPLES</span></span>

### <span data-ttu-id="87139-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="87139-108">Example 1</span></span>
```powershell
PS C:\> Set-AzureRmCognitiveServicesAccount -ResourceGroupName cognitive-services-resource-group -name myluis -SkuName S0


ResourceGroupName : cognitive-services-resource-group
AccountName       : myluis
Id                : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/cognitive-services-resource-group/providers/Microsoft.Cog
                    nitiveServices/accounts/myluis
Endpoint          : https://westus.api.cognitive.microsoft.com/luis/v2.0
Location          : WESTUS
Sku               : Microsoft.Azure.Management.CognitiveServices.Models.Sku
AccountType       : LUIS
ResourceType      : Microsoft.CognitiveServices/accounts
Etag              : "xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx"
ProvisioningState : Succeeded
Tags              :
```

## <span data-ttu-id="87139-109">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="87139-109">PARAMETERS</span></span>

### <span data-ttu-id="87139-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="87139-110">-DefaultProfile</span></span>
<span data-ttu-id="87139-111">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="87139-111">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="87139-112">-Force</span><span class="sxs-lookup"><span data-stu-id="87139-112">-Force</span></span>
<span data-ttu-id="87139-113">Wymusza uruchomienie polecenia bez monitowania o potwierdzenie użytkownika.</span><span class="sxs-lookup"><span data-stu-id="87139-113">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="87139-114">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="87139-114">-Name</span></span>
<span data-ttu-id="87139-115">Określa nazwę konta, które ma zostać zmodyfikowane.</span><span class="sxs-lookup"><span data-stu-id="87139-115">Specifies the name of the account to modify.</span></span>

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

### <span data-ttu-id="87139-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="87139-116">-ResourceGroupName</span></span>
<span data-ttu-id="87139-117">Określa nazwę grupy zasobów, do której przypisano konto.</span><span class="sxs-lookup"><span data-stu-id="87139-117">Specifies the name of the resource group the account is assigned to.</span></span>

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

### <span data-ttu-id="87139-118">-SkuName</span><span class="sxs-lookup"><span data-stu-id="87139-118">-SkuName</span></span>
<span data-ttu-id="87139-119">Określa jednostkę SKU konta.</span><span class="sxs-lookup"><span data-stu-id="87139-119">Specifies the SKU for the account.</span></span>
<span data-ttu-id="87139-120">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="87139-120">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="87139-121">F0 (warstwa wolna)</span><span class="sxs-lookup"><span data-stu-id="87139-121">F0 (free tier)</span></span>
- <span data-ttu-id="87139-122">S0</span><span class="sxs-lookup"><span data-stu-id="87139-122">S0</span></span>
- <span data-ttu-id="87139-123">S1</span><span class="sxs-lookup"><span data-stu-id="87139-123">S1</span></span>
- <span data-ttu-id="87139-124">S2</span><span class="sxs-lookup"><span data-stu-id="87139-124">S2</span></span>
- <span data-ttu-id="87139-125">S3</span><span class="sxs-lookup"><span data-stu-id="87139-125">S3</span></span>
- <span data-ttu-id="87139-126">Stanu</span><span class="sxs-lookup"><span data-stu-id="87139-126">S4</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="87139-127">-Tag</span><span class="sxs-lookup"><span data-stu-id="87139-127">-Tag</span></span>
<span data-ttu-id="87139-128">Określa tag jako parę nazwa/wartość.</span><span class="sxs-lookup"><span data-stu-id="87139-128">Specifies a tag as a name/value pair.</span></span>

```yaml
Type: System.Collections.Hashtable[]
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="87139-129">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="87139-129">-Confirm</span></span>
<span data-ttu-id="87139-130">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="87139-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="87139-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="87139-131">-WhatIf</span></span>
<span data-ttu-id="87139-132">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="87139-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="87139-133">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="87139-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="87139-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="87139-134">CommonParameters</span></span>
<span data-ttu-id="87139-135">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="87139-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="87139-136">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="87139-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="87139-137">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="87139-137">INPUTS</span></span>

### <span data-ttu-id="87139-138">System. String</span><span class="sxs-lookup"><span data-stu-id="87139-138">System.String</span></span>

### <span data-ttu-id="87139-139">System. Collections. Hashtable []</span><span class="sxs-lookup"><span data-stu-id="87139-139">System.Collections.Hashtable[]</span></span>

## <span data-ttu-id="87139-140">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="87139-140">OUTPUTS</span></span>

### <span data-ttu-id="87139-141">Microsoft. Azure. Commands. Management. CognitiveServices. models. PSCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="87139-141">Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSCognitiveServicesAccount</span></span>

## <span data-ttu-id="87139-142">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="87139-142">NOTES</span></span>

## <span data-ttu-id="87139-143">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="87139-143">RELATED LINKS</span></span>

[<span data-ttu-id="87139-144">Get-AzureRmCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="87139-144">Get-AzureRmCognitiveServicesAccount</span></span>](./Get-AzureRmCognitiveServicesAccount.md)

[<span data-ttu-id="87139-145">Nowe — AzureRmCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="87139-145">New-AzureRmCognitiveServicesAccount</span></span>](./New-AzureRmCognitiveServicesAccount.md)

[<span data-ttu-id="87139-146">Remove-AzureRmCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="87139-146">Remove-AzureRmCognitiveServicesAccount</span></span>](./Remove-AzureRmCognitiveServicesAccount.md)
