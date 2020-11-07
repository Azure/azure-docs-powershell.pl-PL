---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CognitiveServices.dll-Help.xml
Module Name: Az.CognitiveServices
ms.assetid: 11D5BFDF-5E5D-46B2-9F9B-A0524EFA1B42
online version: https://docs.microsoft.com/en-us/powershell/module/az.cognitiveservices/get-azcognitiveservicesaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CognitiveServices/CognitiveServices/help/Get-AzCognitiveServicesAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CognitiveServices/CognitiveServices/help/Get-AzCognitiveServicesAccount.md
ms.openlocfilehash: 35815afe33329ebfae92638f47176043bf6f5844
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93706519"
---
# <span data-ttu-id="db8dd-101">Get-AzCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="db8dd-101">Get-AzCognitiveServicesAccount</span></span>

## <span data-ttu-id="db8dd-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="db8dd-102">SYNOPSIS</span></span>
<span data-ttu-id="db8dd-103">Pobiera konto.</span><span class="sxs-lookup"><span data-stu-id="db8dd-103">Gets an account.</span></span>

## <span data-ttu-id="db8dd-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="db8dd-104">SYNTAX</span></span>

### <span data-ttu-id="db8dd-105">ResourceGroupParameterSet</span><span class="sxs-lookup"><span data-stu-id="db8dd-105">ResourceGroupParameterSet</span></span>
```
Get-AzCognitiveServicesAccount [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="db8dd-106">AccountNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="db8dd-106">AccountNameParameterSet</span></span>
```
Get-AzCognitiveServicesAccount [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="db8dd-107">Opis</span><span class="sxs-lookup"><span data-stu-id="db8dd-107">DESCRIPTION</span></span>
<span data-ttu-id="db8dd-108">Polecenie cmdlet **Get-AzCognitiveServicesAccount** pobiera konta usług poznawczych w grupie zasobów określonym przez parametr *ResourceGroupName* .</span><span class="sxs-lookup"><span data-stu-id="db8dd-108">The **Get-AzCognitiveServicesAccount** cmdlet gets the provisioned Cognitive Services accounts in the resource group specified by the *ResourceGroupName* parameter.</span></span>
<span data-ttu-id="db8dd-109">Jeśli nie określisz parametru *ResourceGroupName* , to polecenie cmdlet otrzyma wszystkie konta usług poznawczych dla bieżącego abonamentu.</span><span class="sxs-lookup"><span data-stu-id="db8dd-109">If you do not specify the *ResourceGroupName* parameter, this cmdlet gets all Cognitive Services accounts for the current subscription.</span></span>

## <span data-ttu-id="db8dd-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="db8dd-110">EXAMPLES</span></span>

### <span data-ttu-id="db8dd-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="db8dd-111">Example 1</span></span>
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

## <span data-ttu-id="db8dd-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="db8dd-112">PARAMETERS</span></span>

### <span data-ttu-id="db8dd-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="db8dd-113">-DefaultProfile</span></span>
<span data-ttu-id="db8dd-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="db8dd-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="db8dd-115">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="db8dd-115">-Name</span></span>
<span data-ttu-id="db8dd-116">Określa nazwę konta usług poznawczych, które ma zostać pozyskane.</span><span class="sxs-lookup"><span data-stu-id="db8dd-116">Specifies the name of the Cognitive Services account to get.</span></span>

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

### <span data-ttu-id="db8dd-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="db8dd-117">-ResourceGroupName</span></span>
<span data-ttu-id="db8dd-118">Określa nazwę grupy zasobów, do której przypisano konto usług poznawczych.</span><span class="sxs-lookup"><span data-stu-id="db8dd-118">Specifies the name of the resource group the Cognitive Services account is assigned to.</span></span>

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

### <span data-ttu-id="db8dd-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="db8dd-119">CommonParameters</span></span>
<span data-ttu-id="db8dd-120">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="db8dd-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="db8dd-121">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="db8dd-121">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="db8dd-122">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="db8dd-122">INPUTS</span></span>

### <span data-ttu-id="db8dd-123">System. String</span><span class="sxs-lookup"><span data-stu-id="db8dd-123">System.String</span></span>

## <span data-ttu-id="db8dd-124">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="db8dd-124">OUTPUTS</span></span>

### <span data-ttu-id="db8dd-125">Microsoft. Azure. Commands. Management. CognitiveServices. models. PSCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="db8dd-125">Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSCognitiveServicesAccount</span></span>

## <span data-ttu-id="db8dd-126">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="db8dd-126">NOTES</span></span>

## <span data-ttu-id="db8dd-127">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="db8dd-127">RELATED LINKS</span></span>

[<span data-ttu-id="db8dd-128">Nowe — AzCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="db8dd-128">New-AzCognitiveServicesAccount</span></span>](./New-AzCognitiveServicesAccount.md)

[<span data-ttu-id="db8dd-129">Remove-AzCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="db8dd-129">Remove-AzCognitiveServicesAccount</span></span>](./Remove-AzCognitiveServicesAccount.md)

[<span data-ttu-id="db8dd-130">Set-AzCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="db8dd-130">Set-AzCognitiveServicesAccount</span></span>](./Set-AzCognitiveServicesAccount.md)


