---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 45D55DC9-0027-4EB9-B2F7-9ABF6685E6B5
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmAvailabilitySet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmAvailabilitySet.md
ms.openlocfilehash: 769cb913c04c435071c6b743f0d3de533128986f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93553379"
---
# <span data-ttu-id="81d4f-101">Get-AzureRmAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="81d4f-101">Get-AzureRmAvailabilitySet</span></span>

## <span data-ttu-id="81d4f-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="81d4f-102">SYNOPSIS</span></span>
<span data-ttu-id="81d4f-103">Pobiera zestawy dostępności platformy Azure w grupie zasobów.</span><span class="sxs-lookup"><span data-stu-id="81d4f-103">Gets Azure availability sets in a resource group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="81d4f-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="81d4f-104">SYNTAX</span></span>

```
Get-AzureRmAvailabilitySet [-ResourceGroupName] <String> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="81d4f-105">Opis</span><span class="sxs-lookup"><span data-stu-id="81d4f-105">DESCRIPTION</span></span>
<span data-ttu-id="81d4f-106">Polecenie cmdlet **Get-AzureRmAvailabilitySet** pobiera zestawy dostępności platformy Azure w grupie zasobów.</span><span class="sxs-lookup"><span data-stu-id="81d4f-106">The **Get-AzureRmAvailabilitySet** cmdlet gets Azure availability sets in a resource group.</span></span>
<span data-ttu-id="81d4f-107">Możesz określić nazwę określonego zestawu dostępności, aby uzyskać dostęp.</span><span class="sxs-lookup"><span data-stu-id="81d4f-107">You can specify the name of a specific availability set to get.</span></span>

## <span data-ttu-id="81d4f-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="81d4f-108">EXAMPLES</span></span>

### <span data-ttu-id="81d4f-109">Przykład 1: uzyskiwanie określonego zestawu dostępności</span><span class="sxs-lookup"><span data-stu-id="81d4f-109">Example 1: Get a specific availability set</span></span>
```
PS C:\> Get-AzureRmAvailabilitySet -ResourceGroupName "ResourceGroup11" -Name "AvailabilitySet03"
```

<span data-ttu-id="81d4f-110">To polecenie pobiera zestaw dostępności o nazwie AvailablitySet03 w grupie zasobów o nazwie ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="81d4f-110">This command gets the availability set named AvailablitySet03 in the resource group named ResourceGroup11.</span></span>

### <span data-ttu-id="81d4f-111">Przykład 2: pobieranie wszystkich zestawów dostępności</span><span class="sxs-lookup"><span data-stu-id="81d4f-111">Example 2: Get all availability sets</span></span>
```
PS C:\> Get-AzureRmAvailabilitySet -ResourceGroupName "ResourceGroup11"
```

<span data-ttu-id="81d4f-112">To polecenie pobiera wszystkie zestawy dostępności w grupie zasobów o nazwie ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="81d4f-112">This command gets all the availability sets in the resource group named ResourceGroup11.</span></span>

## <span data-ttu-id="81d4f-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="81d4f-113">PARAMETERS</span></span>

### <span data-ttu-id="81d4f-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="81d4f-114">-DefaultProfile</span></span>
<span data-ttu-id="81d4f-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="81d4f-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="81d4f-116">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="81d4f-116">-Name</span></span>
<span data-ttu-id="81d4f-117">Określa nazwę zestawu dostępności, który jest pobierany przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="81d4f-117">Specifies the name of an availability set that this cmdlet gets.</span></span>

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

### <span data-ttu-id="81d4f-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="81d4f-118">-ResourceGroupName</span></span>
<span data-ttu-id="81d4f-119">Określa nazwę grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="81d4f-119">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="81d4f-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="81d4f-120">CommonParameters</span></span>
<span data-ttu-id="81d4f-121">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="81d4f-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="81d4f-122">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="81d4f-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="81d4f-123">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="81d4f-123">INPUTS</span></span>

## <span data-ttu-id="81d4f-124">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="81d4f-124">OUTPUTS</span></span>

## <span data-ttu-id="81d4f-125">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="81d4f-125">NOTES</span></span>

## <span data-ttu-id="81d4f-126">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="81d4f-126">RELATED LINKS</span></span>

[<span data-ttu-id="81d4f-127">Nowe — AzureRmAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="81d4f-127">New-AzureRmAvailabilitySet</span></span>](./New-AzureRmAvailabilitySet.md)

[<span data-ttu-id="81d4f-128">Remove-AzureRmAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="81d4f-128">Remove-AzureRmAvailabilitySet</span></span>](./Remove-AzureRmAvailabilitySet.md)


