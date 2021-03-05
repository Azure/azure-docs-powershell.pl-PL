---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DevSpaces.dll-Help.xml
Module Name: Az.DevSpaces
online version: https://docs.microsoft.com/powershell/module/az.devspaces/get-azdevspacescontroller
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DevSpaces/DevSpaces/help/Get-AzDevSpacesController.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DevSpaces/DevSpaces/help/Get-AzDevSpacesController.md
ms.openlocfilehash: dd7ba99632cfef493fe3202b2402a938b11fa807
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101960762"
---
# <span data-ttu-id="d67db-101">Get-AzDevSpacesController</span><span class="sxs-lookup"><span data-stu-id="d67db-101">Get-AzDevSpacesController</span></span>

## <span data-ttu-id="d67db-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d67db-102">SYNOPSIS</span></span>
<span data-ttu-id="d67db-103">Pobierz lub przygotuj listę kontrolera Azure DevSpaces.</span><span class="sxs-lookup"><span data-stu-id="d67db-103">Get or list Azure DevSpaces controller.</span></span>

## <span data-ttu-id="d67db-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="d67db-104">SYNTAX</span></span>

### <span data-ttu-id="d67db-105">ListDevSpacesControllerParameterSet (Domyślne)</span><span class="sxs-lookup"><span data-stu-id="d67db-105">ListDevSpacesControllerParameterSet (Default)</span></span>
```
Get-AzDevSpacesController [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="d67db-106">DevSpacesControllerNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="d67db-106">DevSpacesControllerNameParameterSet</span></span>
```
Get-AzDevSpacesController [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d67db-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="d67db-107">DESCRIPTION</span></span>
<span data-ttu-id="d67db-108">Pobierz lub przygotuj listę kontrolera Azure DevSpaces.</span><span class="sxs-lookup"><span data-stu-id="d67db-108">Get or list Azure DevSpaces controller.</span></span>

## <span data-ttu-id="d67db-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="d67db-109">EXAMPLES</span></span>

### <span data-ttu-id="d67db-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="d67db-110">Example 1</span></span>
```powershell
PS C:\> Get-AzDevSpacesController

Name        Resource Group  Location  Provisioning State
----------  --------------  --------  ------------------
devSpaceControllerName   devSpaceResourceGroup     eastus    Succeeded
```

<span data-ttu-id="d67db-111">Lista wszystkich kontrolerów w ramach subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="d67db-111">List all controllers in a subscription.</span></span>

### <span data-ttu-id="d67db-112">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="d67db-112">Example 2</span></span>
```powershell
PS C:\> Get-AzDevSpacesController --ResourceGroupName devSpaceResourceGroup -Name devSpaceControllerName

Name        Resource Group  Location  Provisioning State
----------  --------------  --------  ------------------
devSpaceControllerName   devSpaceResourceGroup     eastus    Succeeded
```

<span data-ttu-id="d67db-113">Uzyskaj kontrolery DevSpaces w ramach subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="d67db-113">Get a DevSpaces controllers in a subscription.</span></span>

## <span data-ttu-id="d67db-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d67db-114">PARAMETERS</span></span>

### <span data-ttu-id="d67db-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d67db-115">-DefaultProfile</span></span>
<span data-ttu-id="d67db-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="d67db-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d67db-117">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="d67db-117">-Name</span></span>
<span data-ttu-id="d67db-118">Nazwa kontrolera DevSpaces.</span><span class="sxs-lookup"><span data-stu-id="d67db-118">DevSpaces controller name.</span></span>

```yaml
Type: System.String
Parameter Sets: DevSpacesControllerNameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d67db-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d67db-119">-ResourceGroupName</span></span>
<span data-ttu-id="d67db-120">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="d67db-120">Resource group name</span></span>

```yaml
Type: System.String
Parameter Sets: ListDevSpacesControllerParameterSet
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: DevSpacesControllerNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d67db-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d67db-121">CommonParameters</span></span>
<span data-ttu-id="d67db-122">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d67db-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d67db-123">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d67db-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d67db-124">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d67db-124">INPUTS</span></span>

### <span data-ttu-id="d67db-125">Brak</span><span class="sxs-lookup"><span data-stu-id="d67db-125">None</span></span>

## <span data-ttu-id="d67db-126">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d67db-126">OUTPUTS</span></span>

### <span data-ttu-id="d67db-127">Microsoft.Azure.Commands.DevSpaces.Models.PSController</span><span class="sxs-lookup"><span data-stu-id="d67db-127">Microsoft.Azure.Commands.DevSpaces.Models.PSController</span></span>

## <span data-ttu-id="d67db-128">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="d67db-128">NOTES</span></span>

## <span data-ttu-id="d67db-129">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="d67db-129">RELATED LINKS</span></span>
