---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 45D55DC9-0027-4EB9-B2F7-9ABF6685E6B5
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/get-azurermavailabilityset
schema: 2.0.0
ms.openlocfilehash: ef00a9e425f67fbfc1ce47746503b574d483598f
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/15/2020
ms.locfileid: "93897693"
---
# <span data-ttu-id="692d6-101">Get-AzureRmAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="692d6-101">Get-AzureRmAvailabilitySet</span></span>

## <span data-ttu-id="692d6-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="692d6-102">SYNOPSIS</span></span>
<span data-ttu-id="692d6-103">Pobiera zestawy dostępności platformy Azure w grupie zasobów.</span><span class="sxs-lookup"><span data-stu-id="692d6-103">Gets Azure availability sets in a resource group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="692d6-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="692d6-104">SYNTAX</span></span>

```
Get-AzureRmAvailabilitySet [-ResourceGroupName] <String> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="692d6-105">Opis</span><span class="sxs-lookup"><span data-stu-id="692d6-105">DESCRIPTION</span></span>
<span data-ttu-id="692d6-106">Polecenie cmdlet **Get-AzureRmAvailabilitySet** pobiera zestawy dostępności platformy Azure w grupie zasobów.</span><span class="sxs-lookup"><span data-stu-id="692d6-106">The **Get-AzureRmAvailabilitySet** cmdlet gets Azure availability sets in a resource group.</span></span>
<span data-ttu-id="692d6-107">Możesz określić nazwę określonego zestawu dostępności, aby uzyskać dostęp.</span><span class="sxs-lookup"><span data-stu-id="692d6-107">You can specify the name of a specific availability set to get.</span></span>

## <span data-ttu-id="692d6-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="692d6-108">EXAMPLES</span></span>

### <span data-ttu-id="692d6-109">Przykład 1: uzyskiwanie określonego zestawu dostępności</span><span class="sxs-lookup"><span data-stu-id="692d6-109">Example 1: Get a specific availability set</span></span>
```
PS C:\> Get-AzureRmAvailabilitySet -ResourceGroupName "ResourceGroup11" -Name "AvailabilitySet03"
```

<span data-ttu-id="692d6-110">To polecenie pobiera zestaw dostępności o nazwie AvailablitySet03 w grupie zasobów o nazwie ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="692d6-110">This command gets the availability set named AvailablitySet03 in the resource group named ResourceGroup11.</span></span>

### <span data-ttu-id="692d6-111">Przykład 2: pobieranie wszystkich zestawów dostępności</span><span class="sxs-lookup"><span data-stu-id="692d6-111">Example 2: Get all availability sets</span></span>
```
PS C:\> Get-AzureRmAvailabilitySet -ResourceGroupName "ResourceGroup11"
```

<span data-ttu-id="692d6-112">To polecenie pobiera wszystkie zestawy dostępności w grupie zasobów o nazwie ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="692d6-112">This command gets all the availability sets in the resource group named ResourceGroup11.</span></span>

## <span data-ttu-id="692d6-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="692d6-113">PARAMETERS</span></span>

### <span data-ttu-id="692d6-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="692d6-114">-DefaultProfile</span></span>
<span data-ttu-id="692d6-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="692d6-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="692d6-116">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="692d6-116">-Name</span></span>
<span data-ttu-id="692d6-117">Określa nazwę zestawu dostępności, który jest pobierany przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="692d6-117">Specifies the name of an availability set that this cmdlet gets.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName, AvailabilitySetName

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="692d6-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="692d6-118">-ResourceGroupName</span></span>
<span data-ttu-id="692d6-119">Określa nazwę grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="692d6-119">Specifies the name of a resource group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="692d6-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="692d6-120">CommonParameters</span></span>
<span data-ttu-id="692d6-121">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="692d6-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="692d6-122">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="692d6-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="692d6-123">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="692d6-123">INPUTS</span></span>

### <span data-ttu-id="692d6-124">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="692d6-124">None</span></span>
<span data-ttu-id="692d6-125">To polecenie cmdlet nie akceptuje żadnych danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="692d6-125">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="692d6-126">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="692d6-126">OUTPUTS</span></span>

### <span data-ttu-id="692d6-127">Microsoft. Azure. Commands. COMPUTE. models. PSAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="692d6-127">Microsoft.Azure.Commands.Compute.Models.PSAvailabilitySet</span></span>

## <span data-ttu-id="692d6-128">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="692d6-128">NOTES</span></span>

## <span data-ttu-id="692d6-129">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="692d6-129">RELATED LINKS</span></span>

[<span data-ttu-id="692d6-130">Nowe — AzureRmAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="692d6-130">New-AzureRmAvailabilitySet</span></span>](./New-AzureRmAvailabilitySet.md)

[<span data-ttu-id="692d6-131">Remove-AzureRmAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="692d6-131">Remove-AzureRmAvailabilitySet</span></span>](./Remove-AzureRmAvailabilitySet.md)


