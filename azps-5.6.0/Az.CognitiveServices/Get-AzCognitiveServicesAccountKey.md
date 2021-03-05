---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CognitiveServices.dll-Help.xml
Module Name: Az.CognitiveServices
ms.assetid: 73B1EB7E-568E-44E8-993A-91678B7D8AEE
online version: https://docs.microsoft.com/powershell/module/az.cognitiveservices/get-azcognitiveservicesaccountkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CognitiveServices/CognitiveServices/help/Get-AzCognitiveServicesAccountKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CognitiveServices/CognitiveServices/help/Get-AzCognitiveServicesAccountKey.md
ms.openlocfilehash: 46da28f86cac8aed68724683aaa69fde8ea64a50
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "102007130"
---
# <span data-ttu-id="f9156-101">Get-AzCognitiveServicesAccountKey</span><span class="sxs-lookup"><span data-stu-id="f9156-101">Get-AzCognitiveServicesAccountKey</span></span>

## <span data-ttu-id="f9156-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f9156-102">SYNOPSIS</span></span>
<span data-ttu-id="f9156-103">Pobiera klucze interfejsu API dla konta.</span><span class="sxs-lookup"><span data-stu-id="f9156-103">Gets the API keys for an account.</span></span>

## <span data-ttu-id="f9156-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="f9156-104">SYNTAX</span></span>

```
Get-AzCognitiveServicesAccountKey [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f9156-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="f9156-105">DESCRIPTION</span></span>
<span data-ttu-id="f9156-106">Polecenie **cmdlet Get-AzCognitiveServicesAccountKey** pobiera klucze interfejsu API dla aprowizowanych kont usług Cognitive Services.</span><span class="sxs-lookup"><span data-stu-id="f9156-106">The **Get-AzCognitiveServicesAccountKey** cmdlet gets the API keys for a provisioned Cognitive Services account.</span></span>
<span data-ttu-id="f9156-107">Konto usług Cognitive Services ma dwa klucze interfejsu API: Key1 i Key2.</span><span class="sxs-lookup"><span data-stu-id="f9156-107">A Cognitive Services account has two API keys: Key1 and Key2.</span></span>
<span data-ttu-id="f9156-108">Klucze umożliwiają interakcję z punktem końcowym konta usług Cognitive Services.</span><span class="sxs-lookup"><span data-stu-id="f9156-108">The keys enable interaction with the Cognitive Services account endpoint.</span></span>
<span data-ttu-id="f9156-109">Użyj New-AzCognitiveServicesAccountKey, aby ponownie wygenerować klucz.</span><span class="sxs-lookup"><span data-stu-id="f9156-109">Use New-AzCognitiveServicesAccountKey to regenerate a key.</span></span>

## <span data-ttu-id="f9156-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="f9156-110">EXAMPLES</span></span>

### <span data-ttu-id="f9156-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="f9156-111">Example 1</span></span>
```powershell
PS C:\> Get-AzCognitiveServicesAccountKey -ResourceGroupName cognitive-services-resource-group -name myluis

Key1                             Key2
----                             ----
xxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxx xxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxx
```

## <span data-ttu-id="f9156-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f9156-112">PARAMETERS</span></span>

### <span data-ttu-id="f9156-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f9156-113">-DefaultProfile</span></span>
<span data-ttu-id="f9156-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="f9156-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f9156-115">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="f9156-115">-Name</span></span>
<span data-ttu-id="f9156-116">Określa nazwę konta.</span><span class="sxs-lookup"><span data-stu-id="f9156-116">Specifies the name of the account.</span></span>
<span data-ttu-id="f9156-117">To polecenie cmdlet pobiera klucze dla tego konta.</span><span class="sxs-lookup"><span data-stu-id="f9156-117">This cmdlet gets the keys for this account.</span></span>

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

### <span data-ttu-id="f9156-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f9156-118">-ResourceGroupName</span></span>
<span data-ttu-id="f9156-119">Określa nazwę grupy zasobów, do których przypisano konto.</span><span class="sxs-lookup"><span data-stu-id="f9156-119">Specifies the name of the resource group the account is assigned to.</span></span>

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

### <span data-ttu-id="f9156-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f9156-120">CommonParameters</span></span>
<span data-ttu-id="f9156-121">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f9156-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f9156-122">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f9156-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f9156-123">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f9156-123">INPUTS</span></span>

### <span data-ttu-id="f9156-124">System.String</span><span class="sxs-lookup"><span data-stu-id="f9156-124">System.String</span></span>

## <span data-ttu-id="f9156-125">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f9156-125">OUTPUTS</span></span>

### <span data-ttu-id="f9156-126">Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSCognitiveServicesAccountKeys</span><span class="sxs-lookup"><span data-stu-id="f9156-126">Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSCognitiveServicesAccountKeys</span></span>

## <span data-ttu-id="f9156-127">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="f9156-127">NOTES</span></span>

## <span data-ttu-id="f9156-128">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="f9156-128">RELATED LINKS</span></span>

[<span data-ttu-id="f9156-129">New-AzCognitiveServicesAccountKey</span><span class="sxs-lookup"><span data-stu-id="f9156-129">New-AzCognitiveServicesAccountKey</span></span>](./New-AzCognitiveServicesAccountKey.md)


