---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CognitiveServices.dll-Help.xml
Module Name: Az.CognitiveServices
ms.assetid: 11E2D82A-1DF1-4E19-8328-44674641D1BB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cognitiveservices/set-azcognitiveservicesaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CognitiveServices/CognitiveServices/help/Set-AzCognitiveServicesAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CognitiveServices/CognitiveServices/help/Set-AzCognitiveServicesAccount.md
ms.openlocfilehash: 2544531d9a988daaea314fc2088609df77b719b7
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93710353"
---
# <span data-ttu-id="3b3ec-101">Set-AzCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="3b3ec-101">Set-AzCognitiveServicesAccount</span></span>

## <span data-ttu-id="3b3ec-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="3b3ec-102">SYNOPSIS</span></span>
<span data-ttu-id="3b3ec-103">Modyfikuje konto.</span><span class="sxs-lookup"><span data-stu-id="3b3ec-103">Modifies an account.</span></span>

## <span data-ttu-id="3b3ec-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="3b3ec-104">SYNTAX</span></span>

```
Set-AzCognitiveServicesAccount [-ResourceGroupName] <String> [-Name] <String> [-SkuName <String>]
 [-Tag <Hashtable[]>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="3b3ec-105">Opis</span><span class="sxs-lookup"><span data-stu-id="3b3ec-105">DESCRIPTION</span></span>
<span data-ttu-id="3b3ec-106">Polecenie cmdlet **Set-AzCognitiveServicesAccount** modyfikuje jednostkę SKU lub Tagi określonego konta usług poznawczych.</span><span class="sxs-lookup"><span data-stu-id="3b3ec-106">The **Set-AzCognitiveServicesAccount** cmdlet modifies the SKU or tags of the specified Cognitive Services account.</span></span>

## <span data-ttu-id="3b3ec-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="3b3ec-107">EXAMPLES</span></span>

### <span data-ttu-id="3b3ec-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="3b3ec-108">Example 1</span></span>
```powershell
PS C:\> Set-AzCognitiveServicesAccount -ResourceGroupName cognitive-services-resource-group -name myluis -SkuName S0


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

## <span data-ttu-id="3b3ec-109">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="3b3ec-109">PARAMETERS</span></span>

### <span data-ttu-id="3b3ec-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3b3ec-110">-DefaultProfile</span></span>
<span data-ttu-id="3b3ec-111">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="3b3ec-111">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="3b3ec-112">-Force</span><span class="sxs-lookup"><span data-stu-id="3b3ec-112">-Force</span></span>
<span data-ttu-id="3b3ec-113">Wymusza uruchomienie polecenia bez monitowania o potwierdzenie użytkownika.</span><span class="sxs-lookup"><span data-stu-id="3b3ec-113">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="3b3ec-114">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="3b3ec-114">-Name</span></span>
<span data-ttu-id="3b3ec-115">Określa nazwę konta, które ma zostać zmodyfikowane.</span><span class="sxs-lookup"><span data-stu-id="3b3ec-115">Specifies the name of the account to modify.</span></span>

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

### <span data-ttu-id="3b3ec-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3b3ec-116">-ResourceGroupName</span></span>
<span data-ttu-id="3b3ec-117">Określa nazwę grupy zasobów, do której przypisano konto.</span><span class="sxs-lookup"><span data-stu-id="3b3ec-117">Specifies the name of the resource group the account is assigned to.</span></span>

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

### <span data-ttu-id="3b3ec-118">-SkuName</span><span class="sxs-lookup"><span data-stu-id="3b3ec-118">-SkuName</span></span>
<span data-ttu-id="3b3ec-119">Określa jednostkę SKU konta.</span><span class="sxs-lookup"><span data-stu-id="3b3ec-119">Specifies the SKU for the account.</span></span>
<span data-ttu-id="3b3ec-120">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="3b3ec-120">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="3b3ec-121">F0 (warstwa wolna)</span><span class="sxs-lookup"><span data-stu-id="3b3ec-121">F0 (free tier)</span></span>
- <span data-ttu-id="3b3ec-122">S0</span><span class="sxs-lookup"><span data-stu-id="3b3ec-122">S0</span></span>
- <span data-ttu-id="3b3ec-123">S1</span><span class="sxs-lookup"><span data-stu-id="3b3ec-123">S1</span></span>
- <span data-ttu-id="3b3ec-124">S2</span><span class="sxs-lookup"><span data-stu-id="3b3ec-124">S2</span></span>
- <span data-ttu-id="3b3ec-125">S3</span><span class="sxs-lookup"><span data-stu-id="3b3ec-125">S3</span></span>
- <span data-ttu-id="3b3ec-126">Stanu</span><span class="sxs-lookup"><span data-stu-id="3b3ec-126">S4</span></span>

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

### <span data-ttu-id="3b3ec-127">-Tag</span><span class="sxs-lookup"><span data-stu-id="3b3ec-127">-Tag</span></span>
<span data-ttu-id="3b3ec-128">Określa tag jako parę nazwa/wartość.</span><span class="sxs-lookup"><span data-stu-id="3b3ec-128">Specifies a tag as a name/value pair.</span></span>

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

### <span data-ttu-id="3b3ec-129">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="3b3ec-129">-Confirm</span></span>
<span data-ttu-id="3b3ec-130">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3b3ec-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3b3ec-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3b3ec-131">-WhatIf</span></span>
<span data-ttu-id="3b3ec-132">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3b3ec-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3b3ec-133">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="3b3ec-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3b3ec-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3b3ec-134">CommonParameters</span></span>
<span data-ttu-id="3b3ec-135">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3b3ec-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3b3ec-136">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3b3ec-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3b3ec-137">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="3b3ec-137">INPUTS</span></span>

### <span data-ttu-id="3b3ec-138">System. String</span><span class="sxs-lookup"><span data-stu-id="3b3ec-138">System.String</span></span>

### <span data-ttu-id="3b3ec-139">System. Collections. Hashtable []</span><span class="sxs-lookup"><span data-stu-id="3b3ec-139">System.Collections.Hashtable[]</span></span>

## <span data-ttu-id="3b3ec-140">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="3b3ec-140">OUTPUTS</span></span>

### <span data-ttu-id="3b3ec-141">Microsoft. Azure. Commands. Management. CognitiveServices. models. PSCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="3b3ec-141">Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSCognitiveServicesAccount</span></span>

## <span data-ttu-id="3b3ec-142">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="3b3ec-142">NOTES</span></span>

## <span data-ttu-id="3b3ec-143">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="3b3ec-143">RELATED LINKS</span></span>

[<span data-ttu-id="3b3ec-144">Get-AzCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="3b3ec-144">Get-AzCognitiveServicesAccount</span></span>](./Get-AzCognitiveServicesAccount.md)

[<span data-ttu-id="3b3ec-145">Nowe — AzCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="3b3ec-145">New-AzCognitiveServicesAccount</span></span>](./New-AzCognitiveServicesAccount.md)

[<span data-ttu-id="3b3ec-146">Remove-AzCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="3b3ec-146">Remove-AzCognitiveServicesAccount</span></span>](./Remove-AzCognitiveServicesAccount.md)
