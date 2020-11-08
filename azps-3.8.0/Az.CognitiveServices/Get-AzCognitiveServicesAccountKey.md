---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CognitiveServices.dll-Help.xml
Module Name: Az.CognitiveServices
ms.assetid: 73B1EB7E-568E-44E8-993A-91678B7D8AEE
online version: https://docs.microsoft.com/en-us/powershell/module/az.cognitiveservices/get-azcognitiveservicesaccountkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CognitiveServices/CognitiveServices/help/Get-AzCognitiveServicesAccountKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CognitiveServices/CognitiveServices/help/Get-AzCognitiveServicesAccountKey.md
ms.openlocfilehash: 8150abc726f990b699237dbaad3641a99bae2e2c
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/21/2020
ms.locfileid: "94049283"
---
# <span data-ttu-id="51470-101">Get-AzCognitiveServicesAccountKey</span><span class="sxs-lookup"><span data-stu-id="51470-101">Get-AzCognitiveServicesAccountKey</span></span>

## <span data-ttu-id="51470-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="51470-102">SYNOPSIS</span></span>
<span data-ttu-id="51470-103">Pobiera klucze interfejsu API dla konta.</span><span class="sxs-lookup"><span data-stu-id="51470-103">Gets the API keys for an account.</span></span>

## <span data-ttu-id="51470-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="51470-104">SYNTAX</span></span>

```
Get-AzCognitiveServicesAccountKey [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="51470-105">Opis</span><span class="sxs-lookup"><span data-stu-id="51470-105">DESCRIPTION</span></span>
<span data-ttu-id="51470-106">Polecenie cmdlet **Get-AzCognitiveServicesAccountKey** pobiera klucze interfejsu API dla konta usług poznawczych.</span><span class="sxs-lookup"><span data-stu-id="51470-106">The **Get-AzCognitiveServicesAccountKey** cmdlet gets the API keys for a provisioned Cognitive Services account.</span></span>
<span data-ttu-id="51470-107">Konto usług poznawczych ma dwa klucze API: KEY1 oraz key2.</span><span class="sxs-lookup"><span data-stu-id="51470-107">A Cognitive Services account has two API keys: Key1 and Key2.</span></span>
<span data-ttu-id="51470-108">Klucze umożliwiają interakcję z punktem końcowym konta usług poznawczych.</span><span class="sxs-lookup"><span data-stu-id="51470-108">The keys enable interaction with the Cognitive Services account endpoint.</span></span>
<span data-ttu-id="51470-109">Aby ponownie wygenerować klucz, użyj New-AzCognitiveServicesAccountKey.</span><span class="sxs-lookup"><span data-stu-id="51470-109">Use New-AzCognitiveServicesAccountKey to regenerate a key.</span></span>

## <span data-ttu-id="51470-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="51470-110">EXAMPLES</span></span>

### <span data-ttu-id="51470-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="51470-111">Example 1</span></span>
```powershell
PS C:\> Get-AzCognitiveServicesAccountKey -ResourceGroupName cognitive-services-resource-group -name myluis

Key1                             Key2
----                             ----
xxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxx xxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxx
```

## <span data-ttu-id="51470-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="51470-112">PARAMETERS</span></span>

### <span data-ttu-id="51470-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="51470-113">-DefaultProfile</span></span>
<span data-ttu-id="51470-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="51470-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="51470-115">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="51470-115">-Name</span></span>
<span data-ttu-id="51470-116">Określa nazwę konta.</span><span class="sxs-lookup"><span data-stu-id="51470-116">Specifies the name of the account.</span></span>
<span data-ttu-id="51470-117">To polecenie cmdlet umożliwia pobieranie kluczy dla tego konta.</span><span class="sxs-lookup"><span data-stu-id="51470-117">This cmdlet gets the keys for this account.</span></span>

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

### <span data-ttu-id="51470-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="51470-118">-ResourceGroupName</span></span>
<span data-ttu-id="51470-119">Określa nazwę grupy zasobów, do której przypisano konto.</span><span class="sxs-lookup"><span data-stu-id="51470-119">Specifies the name of the resource group the account is assigned to.</span></span>

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

### <span data-ttu-id="51470-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="51470-120">CommonParameters</span></span>
<span data-ttu-id="51470-121">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="51470-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="51470-122">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="51470-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="51470-123">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="51470-123">INPUTS</span></span>

### <span data-ttu-id="51470-124">System. String</span><span class="sxs-lookup"><span data-stu-id="51470-124">System.String</span></span>

## <span data-ttu-id="51470-125">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="51470-125">OUTPUTS</span></span>

### <span data-ttu-id="51470-126">Microsoft. Azure. Commands. Management. CognitiveServices. models. PSCognitiveServicesAccountKeys</span><span class="sxs-lookup"><span data-stu-id="51470-126">Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSCognitiveServicesAccountKeys</span></span>

## <span data-ttu-id="51470-127">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="51470-127">NOTES</span></span>

## <span data-ttu-id="51470-128">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="51470-128">RELATED LINKS</span></span>

[<span data-ttu-id="51470-129">Nowe — AzCognitiveServicesAccountKey</span><span class="sxs-lookup"><span data-stu-id="51470-129">New-AzCognitiveServicesAccountKey</span></span>](./New-AzCognitiveServicesAccountKey.md)


