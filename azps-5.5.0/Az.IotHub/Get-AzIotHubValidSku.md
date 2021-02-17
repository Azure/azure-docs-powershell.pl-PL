---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/get-aziothubvalidsku
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubValidSku.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubValidSku.md
ms.openlocfilehash: e0f178c10fa74d8fa230472397d7bcc835f98bf4
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100188202"
---
# <span data-ttu-id="18334-101">Get-AzIotHubValidSku</span><span class="sxs-lookup"><span data-stu-id="18334-101">Get-AzIotHubValidSku</span></span>

## <span data-ttu-id="18334-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="18334-102">SYNOPSIS</span></span>
<span data-ttu-id="18334-103">Pobiera wszystkie prawidłowe jednostki SKU, do których może zostać przejście w tej usłudze IotHub.</span><span class="sxs-lookup"><span data-stu-id="18334-103">Gets all valid skus that this IotHub can transition to.</span></span>

## <span data-ttu-id="18334-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="18334-104">SYNTAX</span></span>

```
Get-AzIotHubValidSku [-ResourceGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="18334-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="18334-105">DESCRIPTION</span></span>
<span data-ttu-id="18334-106">Pobiera wszystkie prawidłowe jednostki SKU, do których może zostać przejście w tej usłudze IotHub.</span><span class="sxs-lookup"><span data-stu-id="18334-106">Gets all the valid skus that this IotHub can transition to.</span></span>
<span data-ttu-id="18334-107">Aplikacja IotHub nie może przechodzić między jednostkami SKU bezpłatnymi i płatnymi i odwrotnie.</span><span class="sxs-lookup"><span data-stu-id="18334-107">An IotHub cannot transition between free and the paid skus and vice versa.</span></span> <span data-ttu-id="18334-108">Aby osiągnąć ten cel, musisz usunąć i ponownie utworzyć tę kartę.</span><span class="sxs-lookup"><span data-stu-id="18334-108">You will have to delete and recreate the iothub if you want to achieve this.</span></span>

## <span data-ttu-id="18334-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="18334-109">EXAMPLES</span></span>

### <span data-ttu-id="18334-110">Przykład 1. Uzyskiwanie prawidłowych jednostki SKU</span><span class="sxs-lookup"><span data-stu-id="18334-110">Example 1 Get the valid skus</span></span>
```
PS C:\> Get-AzIotHubValidSku -ResourceGroupName "myresourcegroup" -Name "myiothub"
```

<span data-ttu-id="18334-111">Pobiera listę wszystkich jednostki SKU dla aplikacji IotHub o nazwie "myiothub"</span><span class="sxs-lookup"><span data-stu-id="18334-111">Gets a list of all skus for the IotHub named "myiothub"</span></span>

## <span data-ttu-id="18334-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="18334-112">PARAMETERS</span></span>

### <span data-ttu-id="18334-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="18334-113">-DefaultProfile</span></span>
<span data-ttu-id="18334-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="18334-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="18334-115">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="18334-115">-Name</span></span>
<span data-ttu-id="18334-116">Nazwa centrum IoT.</span><span class="sxs-lookup"><span data-stu-id="18334-116">Name of the IoT hub.</span></span> 

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

### <span data-ttu-id="18334-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="18334-117">-ResourceGroupName</span></span>
<span data-ttu-id="18334-118">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="18334-118">Resource Group Name</span></span>

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

### <span data-ttu-id="18334-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="18334-119">CommonParameters</span></span>
<span data-ttu-id="18334-120">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="18334-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="18334-121">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="18334-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="18334-122">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="18334-122">INPUTS</span></span>

### <span data-ttu-id="18334-123">System.String</span><span class="sxs-lookup"><span data-stu-id="18334-123">System.String</span></span>

## <span data-ttu-id="18334-124">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="18334-124">OUTPUTS</span></span>

### <span data-ttu-id="18334-125">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubSkuDescription</span><span class="sxs-lookup"><span data-stu-id="18334-125">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubSkuDescription</span></span>

## <span data-ttu-id="18334-126">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="18334-126">NOTES</span></span>

## <span data-ttu-id="18334-127">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="18334-127">RELATED LINKS</span></span>
