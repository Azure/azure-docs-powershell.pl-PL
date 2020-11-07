---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 45D55DC9-0027-4EB9-B2F7-9ABF6685E6B5
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/get-azurermavailabilityset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Get-AzureRmAvailabilitySet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Get-AzureRmAvailabilitySet.md
ms.openlocfilehash: 685dafeb72693a617ca627aa1abcae19c5e24389
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93541903"
---
# <span data-ttu-id="471b8-101">Get-AzureRmAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="471b8-101">Get-AzureRmAvailabilitySet</span></span>

## <span data-ttu-id="471b8-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="471b8-102">SYNOPSIS</span></span>
<span data-ttu-id="471b8-103">Pobiera zestawy dostępności platformy Azure w grupie zasobów.</span><span class="sxs-lookup"><span data-stu-id="471b8-103">Gets Azure availability sets in a resource group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="471b8-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="471b8-104">SYNTAX</span></span>

```
Get-AzureRmAvailabilitySet [[-ResourceGroupName] <String>] [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="471b8-105">Opis</span><span class="sxs-lookup"><span data-stu-id="471b8-105">DESCRIPTION</span></span>
<span data-ttu-id="471b8-106">Polecenie cmdlet **Get-AzureRmAvailabilitySet** pobiera zestawy dostępności platformy Azure w grupie zasobów.</span><span class="sxs-lookup"><span data-stu-id="471b8-106">The **Get-AzureRmAvailabilitySet** cmdlet gets Azure availability sets in a resource group.</span></span>
<span data-ttu-id="471b8-107">Możesz określić nazwę określonego zestawu dostępności, aby uzyskać dostęp.</span><span class="sxs-lookup"><span data-stu-id="471b8-107">You can specify the name of a specific availability set to get.</span></span>

## <span data-ttu-id="471b8-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="471b8-108">EXAMPLES</span></span>

### <span data-ttu-id="471b8-109">Przykład 1: uzyskiwanie określonego zestawu dostępności</span><span class="sxs-lookup"><span data-stu-id="471b8-109">Example 1: Get a specific availability set</span></span>
```
PS C:\> Get-AzureRmAvailabilitySet -ResourceGroupName "ResourceGroup11" -Name "AvailabilitySet03"
```

<span data-ttu-id="471b8-110">To polecenie pobiera zestaw dostępności o nazwie AvailablitySet03 w grupie zasobów o nazwie ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="471b8-110">This command gets the availability set named AvailablitySet03 in the resource group named ResourceGroup11.</span></span>

### <span data-ttu-id="471b8-111">Przykład 2: pobieranie wszystkich zestawów dostępności</span><span class="sxs-lookup"><span data-stu-id="471b8-111">Example 2: Get all availability sets</span></span>
```
PS C:\> Get-AzureRmAvailabilitySet -ResourceGroupName "ResourceGroup11"
```

<span data-ttu-id="471b8-112">To polecenie pobiera wszystkie zestawy dostępności w grupie zasobów o nazwie ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="471b8-112">This command gets all the availability sets in the resource group named ResourceGroup11.</span></span>

## <span data-ttu-id="471b8-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="471b8-113">PARAMETERS</span></span>

### <span data-ttu-id="471b8-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="471b8-114">-DefaultProfile</span></span>
<span data-ttu-id="471b8-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="471b8-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="471b8-116">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="471b8-116">-Name</span></span>
<span data-ttu-id="471b8-117">Określa nazwę zestawu dostępności, który jest pobierany przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="471b8-117">Specifies the name of an availability set that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName, AvailabilitySetName

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="471b8-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="471b8-118">-ResourceGroupName</span></span>
<span data-ttu-id="471b8-119">Określa nazwę grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="471b8-119">Specifies the name of a resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="471b8-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="471b8-120">CommonParameters</span></span>
<span data-ttu-id="471b8-121">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="471b8-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="471b8-122">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="471b8-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="471b8-123">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="471b8-123">INPUTS</span></span>

### <span data-ttu-id="471b8-124">System. String</span><span class="sxs-lookup"><span data-stu-id="471b8-124">System.String</span></span>

## <span data-ttu-id="471b8-125">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="471b8-125">OUTPUTS</span></span>

### <span data-ttu-id="471b8-126">Microsoft. Azure. Commands. COMPUTE. models. PSAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="471b8-126">Microsoft.Azure.Commands.Compute.Models.PSAvailabilitySet</span></span>

## <span data-ttu-id="471b8-127">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="471b8-127">NOTES</span></span>

## <span data-ttu-id="471b8-128">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="471b8-128">RELATED LINKS</span></span>

[<span data-ttu-id="471b8-129">Nowe — AzureRmAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="471b8-129">New-AzureRmAvailabilitySet</span></span>](./New-AzureRmAvailabilitySet.md)

[<span data-ttu-id="471b8-130">Remove-AzureRmAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="471b8-130">Remove-AzureRmAvailabilitySet</span></span>](./Remove-AzureRmAvailabilitySet.md)

