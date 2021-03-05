---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/powershell/module/az.iothub/get-aziothubvalidsku
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubValidSku.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubValidSku.md
ms.openlocfilehash: b51c41ddd36d19afedd0091be9b0a00bb447faaa
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101964618"
---
# <span data-ttu-id="83c0e-101">Get-AzIotHubValidSku</span><span class="sxs-lookup"><span data-stu-id="83c0e-101">Get-AzIotHubValidSku</span></span>

## <span data-ttu-id="83c0e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="83c0e-102">SYNOPSIS</span></span>
<span data-ttu-id="83c0e-103">Pobiera wszystkie prawidłowe jednostki SKU, do których może zostać przejście w tej usłudze IotHub.</span><span class="sxs-lookup"><span data-stu-id="83c0e-103">Gets all valid skus that this IotHub can transition to.</span></span>

## <span data-ttu-id="83c0e-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="83c0e-104">SYNTAX</span></span>

```
Get-AzIotHubValidSku [-ResourceGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="83c0e-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="83c0e-105">DESCRIPTION</span></span>
<span data-ttu-id="83c0e-106">Pobiera wszystkie prawidłowe jednostki SKU, do których może zostać przejście w tej usłudze IotHub.</span><span class="sxs-lookup"><span data-stu-id="83c0e-106">Gets all the valid skus that this IotHub can transition to.</span></span>
<span data-ttu-id="83c0e-107">Aplikacja IotHub nie może przechodzić między jednostkami SKU bezpłatnymi i płatnymi i odwrotnie.</span><span class="sxs-lookup"><span data-stu-id="83c0e-107">An IotHub cannot transition between free and the paid skus and vice versa.</span></span> <span data-ttu-id="83c0e-108">Aby osiągnąć ten cel, musisz usunąć i ponownie utworzyć tę kartę.</span><span class="sxs-lookup"><span data-stu-id="83c0e-108">You will have to delete and recreate the iothub if you want to achieve this.</span></span>

## <span data-ttu-id="83c0e-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="83c0e-109">EXAMPLES</span></span>

### <span data-ttu-id="83c0e-110">Przykład 1. Uzyskiwanie prawidłowych jednostki SKU</span><span class="sxs-lookup"><span data-stu-id="83c0e-110">Example 1 Get the valid skus</span></span>
```
PS C:\> Get-AzIotHubValidSku -ResourceGroupName "myresourcegroup" -Name "myiothub"
```

<span data-ttu-id="83c0e-111">Pobiera listę wszystkich jednostki SKU dla aplikacji IotHub o nazwie "myiothub"</span><span class="sxs-lookup"><span data-stu-id="83c0e-111">Gets a list of all skus for the IotHub named "myiothub"</span></span>

## <span data-ttu-id="83c0e-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="83c0e-112">PARAMETERS</span></span>

### <span data-ttu-id="83c0e-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="83c0e-113">-DefaultProfile</span></span>
<span data-ttu-id="83c0e-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="83c0e-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="83c0e-115">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="83c0e-115">-Name</span></span>
<span data-ttu-id="83c0e-116">Nazwa centrum IoT.</span><span class="sxs-lookup"><span data-stu-id="83c0e-116">Name of the IoT hub.</span></span> 

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

### <span data-ttu-id="83c0e-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="83c0e-117">-ResourceGroupName</span></span>
<span data-ttu-id="83c0e-118">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="83c0e-118">Resource Group Name</span></span>

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

### <span data-ttu-id="83c0e-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="83c0e-119">CommonParameters</span></span>
<span data-ttu-id="83c0e-120">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="83c0e-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="83c0e-121">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="83c0e-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="83c0e-122">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="83c0e-122">INPUTS</span></span>

### <span data-ttu-id="83c0e-123">System.String</span><span class="sxs-lookup"><span data-stu-id="83c0e-123">System.String</span></span>

## <span data-ttu-id="83c0e-124">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="83c0e-124">OUTPUTS</span></span>

### <span data-ttu-id="83c0e-125">Microsoft.Azure.Commands.Management.iotHub.Models.PSIotHubSkuDescription</span><span class="sxs-lookup"><span data-stu-id="83c0e-125">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubSkuDescription</span></span>

## <span data-ttu-id="83c0e-126">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="83c0e-126">NOTES</span></span>

## <span data-ttu-id="83c0e-127">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="83c0e-127">RELATED LINKS</span></span>
