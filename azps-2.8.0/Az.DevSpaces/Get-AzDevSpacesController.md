---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DevSpaces.dll-Help.xml
Module Name: Az.DevSpaces
online version: https://docs.microsoft.com/en-us/powershell/module/az.devspaces/get-azdevspacescontroller
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DevSpaces/DevSpaces/help/Get-AzDevSpacesController.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DevSpaces/DevSpaces/help/Get-AzDevSpacesController.md
ms.openlocfilehash: 7cc4c61073b0b196faca8d95bd5153abe2587ee7
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93705591"
---
# <span data-ttu-id="7d78e-101">Get-AzDevSpacesController</span><span class="sxs-lookup"><span data-stu-id="7d78e-101">Get-AzDevSpacesController</span></span>

## <span data-ttu-id="7d78e-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="7d78e-102">SYNOPSIS</span></span>
<span data-ttu-id="7d78e-103">Uzyskaj lub wystaw kontroler DevSpaces platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="7d78e-103">Get or list Azure DevSpaces controller.</span></span>

## <span data-ttu-id="7d78e-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="7d78e-104">SYNTAX</span></span>

### <span data-ttu-id="7d78e-105">ListDevSpacesControllerParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="7d78e-105">ListDevSpacesControllerParameterSet (Default)</span></span>
```
Get-AzDevSpacesController [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="7d78e-106">DevSpacesControllerNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="7d78e-106">DevSpacesControllerNameParameterSet</span></span>
```
Get-AzDevSpacesController [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7d78e-107">Opis</span><span class="sxs-lookup"><span data-stu-id="7d78e-107">DESCRIPTION</span></span>
<span data-ttu-id="7d78e-108">Uzyskaj lub wystaw kontroler DevSpaces platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="7d78e-108">Get or list Azure DevSpaces controller.</span></span>

## <span data-ttu-id="7d78e-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="7d78e-109">EXAMPLES</span></span>

### <span data-ttu-id="7d78e-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="7d78e-110">Example 1</span></span>
```powershell
PS C:\> Get-AzDevSpacesController

Name        Resource Group  Location  Provisioning State
----------  --------------  --------  ------------------
devSpaceControllerName   devSpaceResourceGroup     eastus    Succeeded
```

<span data-ttu-id="7d78e-111">Lista wszystkich kontrolerów w ramach abonamentu.</span><span class="sxs-lookup"><span data-stu-id="7d78e-111">List all controllers in a subscription.</span></span>

### <span data-ttu-id="7d78e-112">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="7d78e-112">Example 2</span></span>
```powershell
PS C:\> Get-AzDevSpacesController --ResourceGroupName devSpaceResourceGroup -Name devSpaceControllerName

Name        Resource Group  Location  Provisioning State
----------  --------------  --------  ------------------
devSpaceControllerName   devSpaceResourceGroup     eastus    Succeeded
```

<span data-ttu-id="7d78e-113">Uzyskaj kontrolery DevSpaces w ramach abonamentu.</span><span class="sxs-lookup"><span data-stu-id="7d78e-113">Get a DevSpaces controllers in a subscription.</span></span>

## <span data-ttu-id="7d78e-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="7d78e-114">PARAMETERS</span></span>

### <span data-ttu-id="7d78e-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7d78e-115">-DefaultProfile</span></span>
<span data-ttu-id="7d78e-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="7d78e-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7d78e-117">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="7d78e-117">-Name</span></span>
<span data-ttu-id="7d78e-118">Nazwa kontrolera DevSpaces.</span><span class="sxs-lookup"><span data-stu-id="7d78e-118">DevSpaces controller name.</span></span>

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

### <span data-ttu-id="7d78e-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7d78e-119">-ResourceGroupName</span></span>
<span data-ttu-id="7d78e-120">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="7d78e-120">Resource group name</span></span>

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

### <span data-ttu-id="7d78e-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7d78e-121">CommonParameters</span></span>
<span data-ttu-id="7d78e-122">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7d78e-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7d78e-123">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7d78e-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7d78e-124">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="7d78e-124">INPUTS</span></span>

### <span data-ttu-id="7d78e-125">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="7d78e-125">None</span></span>

## <span data-ttu-id="7d78e-126">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="7d78e-126">OUTPUTS</span></span>

### <span data-ttu-id="7d78e-127">Microsoft. Azure. Commands. DevSpaces. models. PSController</span><span class="sxs-lookup"><span data-stu-id="7d78e-127">Microsoft.Azure.Commands.DevSpaces.Models.PSController</span></span>

## <span data-ttu-id="7d78e-128">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="7d78e-128">NOTES</span></span>

## <span data-ttu-id="7d78e-129">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="7d78e-129">RELATED LINKS</span></span>
