---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CognitiveServices.dll-Help.xml
Module Name: Az.CognitiveServices
ms.assetid: 11D5BFDF-5E5D-46B2-9F9B-A0524EFA1B42
online version: https://docs.microsoft.com/en-us/powershell/module/az.cognitiveservices/get-azcognitiveservicesaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CognitiveServices/CognitiveServices/help/Get-AzCognitiveServicesAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CognitiveServices/CognitiveServices/help/Get-AzCognitiveServicesAccount.md
ms.openlocfilehash: 3f442cc975c6fdbb95d53153c2c80615bb8676a4
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100195106"
---
# <span data-ttu-id="76a44-101">Get-AzCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="76a44-101">Get-AzCognitiveServicesAccount</span></span>

## <span data-ttu-id="76a44-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="76a44-102">SYNOPSIS</span></span>
<span data-ttu-id="76a44-103">Otrzymuje konto.</span><span class="sxs-lookup"><span data-stu-id="76a44-103">Gets an account.</span></span>

## <span data-ttu-id="76a44-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="76a44-104">SYNTAX</span></span>

### <span data-ttu-id="76a44-105">ResourceGroupParameterSet</span><span class="sxs-lookup"><span data-stu-id="76a44-105">ResourceGroupParameterSet</span></span>
```
Get-AzCognitiveServicesAccount [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="76a44-106">AccountNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="76a44-106">AccountNameParameterSet</span></span>
```
Get-AzCognitiveServicesAccount [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="76a44-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="76a44-107">DESCRIPTION</span></span>
<span data-ttu-id="76a44-108">Polecenie **cmdlet Get-AzCognitiveServicesAccount** pobiera aprowizowane konta usług Cognitive Services w grupie zasobów określonej przez parametr *ResourceGroupName.*</span><span class="sxs-lookup"><span data-stu-id="76a44-108">The **Get-AzCognitiveServicesAccount** cmdlet gets the provisioned Cognitive Services accounts in the resource group specified by the *ResourceGroupName* parameter.</span></span>
<span data-ttu-id="76a44-109">Jeśli nie określisz parametru *ResourceGroupName,* to polecenie cmdlet pobiera wszystkie konta usług Cognitive Services dla bieżącej subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="76a44-109">If you do not specify the *ResourceGroupName* parameter, this cmdlet gets all Cognitive Services accounts for the current subscription.</span></span>

## <span data-ttu-id="76a44-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="76a44-110">EXAMPLES</span></span>

### <span data-ttu-id="76a44-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="76a44-111">Example 1</span></span>
```powershell
PS C:\> New-AzCognitiveServicesAccount -ResourceGroupName cognitive-services-resource-group -name myluis -Type LUIS -SkuName S0 -Locati
on 'WestUS'

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

## <span data-ttu-id="76a44-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="76a44-112">PARAMETERS</span></span>

### <span data-ttu-id="76a44-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="76a44-113">-DefaultProfile</span></span>
<span data-ttu-id="76a44-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="76a44-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="76a44-115">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="76a44-115">-Name</span></span>
<span data-ttu-id="76a44-116">Określa nazwę konta usług cognitive services do uzyskania.</span><span class="sxs-lookup"><span data-stu-id="76a44-116">Specifies the name of the Cognitive Services account to get.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountNameParameterSet
Aliases: CognitiveServicesAccountName, AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="76a44-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="76a44-117">-ResourceGroupName</span></span>
<span data-ttu-id="76a44-118">Określa nazwę grupy zasobów, do których jest przypisane konto usług Cognitive Services.</span><span class="sxs-lookup"><span data-stu-id="76a44-118">Specifies the name of the resource group the Cognitive Services account is assigned to.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupParameterSet
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: AccountNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="76a44-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="76a44-119">CommonParameters</span></span>
<span data-ttu-id="76a44-120">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="76a44-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="76a44-121">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="76a44-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="76a44-122">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="76a44-122">INPUTS</span></span>

### <span data-ttu-id="76a44-123">System.String</span><span class="sxs-lookup"><span data-stu-id="76a44-123">System.String</span></span>

## <span data-ttu-id="76a44-124">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="76a44-124">OUTPUTS</span></span>

### <span data-ttu-id="76a44-125">Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="76a44-125">Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSCognitiveServicesAccount</span></span>

## <span data-ttu-id="76a44-126">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="76a44-126">NOTES</span></span>

## <span data-ttu-id="76a44-127">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="76a44-127">RELATED LINKS</span></span>

[<span data-ttu-id="76a44-128">New-AzCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="76a44-128">New-AzCognitiveServicesAccount</span></span>](./New-AzCognitiveServicesAccount.md)

[<span data-ttu-id="76a44-129">Remove-AzCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="76a44-129">Remove-AzCognitiveServicesAccount</span></span>](./Remove-AzCognitiveServicesAccount.md)

[<span data-ttu-id="76a44-130">Set-AzCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="76a44-130">Set-AzCognitiveServicesAccount</span></span>](./Set-AzCognitiveServicesAccount.md)


