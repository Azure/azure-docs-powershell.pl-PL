---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/get-aziothubvalidsku
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubValidSku.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubValidSku.md
ms.openlocfilehash: f81419f43defdf2c66d2d8f1768c63fc09ff0d35
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93868096"
---
# <span data-ttu-id="aec70-101">Get-AzIotHubValidSku</span><span class="sxs-lookup"><span data-stu-id="aec70-101">Get-AzIotHubValidSku</span></span>

## <span data-ttu-id="aec70-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="aec70-102">SYNOPSIS</span></span>
<span data-ttu-id="aec70-103">Pobiera wszystkie prawidłowe jednostki SKU, do których ta IotHub może przejść.</span><span class="sxs-lookup"><span data-stu-id="aec70-103">Gets all valid skus that this IotHub can transition to.</span></span>

## <span data-ttu-id="aec70-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="aec70-104">SYNTAX</span></span>

```
Get-AzIotHubValidSku [-ResourceGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="aec70-105">Opis</span><span class="sxs-lookup"><span data-stu-id="aec70-105">DESCRIPTION</span></span>
<span data-ttu-id="aec70-106">Pobiera wszystkie prawidłowe jednostki SKU, do których ta IotHub może przejść.</span><span class="sxs-lookup"><span data-stu-id="aec70-106">Gets all the valid skus that this IotHub can transition to.</span></span>
<span data-ttu-id="aec70-107">IotHub nie może przechodzić między bezpłatnymi i płatnymi jednostkami SKU oraz odwrotnie.</span><span class="sxs-lookup"><span data-stu-id="aec70-107">An IotHub cannot transition between free and the paid skus and vice versa.</span></span> <span data-ttu-id="aec70-108">Jeśli chcesz to zrobić, musisz usunąć i ponownie utworzyć iothub.</span><span class="sxs-lookup"><span data-stu-id="aec70-108">You will have to delete and recreate the iothub if you want to achieve this.</span></span>

## <span data-ttu-id="aec70-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="aec70-109">EXAMPLES</span></span>

### <span data-ttu-id="aec70-110">Przykład 1 pobieranie prawidłowych wersji SKU</span><span class="sxs-lookup"><span data-stu-id="aec70-110">Example 1 Get the valid skus</span></span>
```
PS C:\> Get-AzIotHubValidSku -ResourceGroupName "myresourcegroup" -Name "myiothub"
```

<span data-ttu-id="aec70-111">Pobiera listę wszystkich wersji SKU dla IotHub o nazwie "myiothub".</span><span class="sxs-lookup"><span data-stu-id="aec70-111">Gets a list of all skus for the IotHub named "myiothub"</span></span>

## <span data-ttu-id="aec70-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="aec70-112">PARAMETERS</span></span>

### <span data-ttu-id="aec70-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aec70-113">-DefaultProfile</span></span>
<span data-ttu-id="aec70-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="aec70-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="aec70-115">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="aec70-115">-Name</span></span>
<span data-ttu-id="aec70-116">Nazwa Centrum IoT.</span><span class="sxs-lookup"><span data-stu-id="aec70-116">Name of the IoT hub.</span></span> 

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="aec70-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="aec70-117">-ResourceGroupName</span></span>
<span data-ttu-id="aec70-118">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="aec70-118">Resource Group Name</span></span>

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

### <span data-ttu-id="aec70-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aec70-119">CommonParameters</span></span>
<span data-ttu-id="aec70-120">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="aec70-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aec70-121">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="aec70-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aec70-122">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="aec70-122">INPUTS</span></span>

### <span data-ttu-id="aec70-123">System. String</span><span class="sxs-lookup"><span data-stu-id="aec70-123">System.String</span></span>

## <span data-ttu-id="aec70-124">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="aec70-124">OUTPUTS</span></span>

### <span data-ttu-id="aec70-125">Microsoft. Azure. Commands. Management. IotHub. models. PSIotHubSkuDescription</span><span class="sxs-lookup"><span data-stu-id="aec70-125">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubSkuDescription</span></span>

## <span data-ttu-id="aec70-126">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="aec70-126">NOTES</span></span>

## <span data-ttu-id="aec70-127">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="aec70-127">RELATED LINKS</span></span>
