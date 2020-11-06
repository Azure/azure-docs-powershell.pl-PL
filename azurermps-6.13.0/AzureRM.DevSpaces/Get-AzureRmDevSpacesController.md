---
external help file: Microsoft.Azure.Commands.DevSpaces.dll-Help.xml
Module Name: AzureRM.DevSpaces
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.devspaces/get-azureevspacescontroller
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DevSpaces/Commands.DevSpaces/help/Get-AzureRmDevSpacesController.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DevSpaces/Commands.DevSpaces/help/Get-AzureRmDevSpacesController.md
ms.openlocfilehash: d0140af9d5345e9f3f68c212ae43403fc0f64280
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93543880"
---
# <span data-ttu-id="a11d5-101">Get-AzureRmDevSpacesController</span><span class="sxs-lookup"><span data-stu-id="a11d5-101">Get-AzureRmDevSpacesController</span></span>

## <span data-ttu-id="a11d5-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="a11d5-102">SYNOPSIS</span></span>
<span data-ttu-id="a11d5-103">Uzyskaj lub wystaw kontroler DevSpaces platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="a11d5-103">Get or list Azure DevSpaces controller.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a11d5-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="a11d5-104">SYNTAX</span></span>

### <span data-ttu-id="a11d5-105">ListDevSpacesControllerParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="a11d5-105">ListDevSpacesControllerParameterSet (Default)</span></span>
```
Get-AzureRmDevSpacesController [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="a11d5-106">DevSpacesControllerNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="a11d5-106">DevSpacesControllerNameParameterSet</span></span>
```
Get-AzureRmDevSpacesController [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a11d5-107">Opis</span><span class="sxs-lookup"><span data-stu-id="a11d5-107">DESCRIPTION</span></span>
<span data-ttu-id="a11d5-108">Uzyskaj lub wystaw kontroler DevSpaces platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="a11d5-108">Get or list Azure DevSpaces controller.</span></span>

## <span data-ttu-id="a11d5-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="a11d5-109">EXAMPLES</span></span>

### <span data-ttu-id="a11d5-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="a11d5-110">Example 1</span></span>
```powershell
PS C:\> Get-AzureRmDevSpacesController

Name        Resource Group  Location  Provisioning State
----------  --------------  --------  ------------------
devSpaceControllerName   devSpaceResourceGroup     eastus    Succeeded
```

<span data-ttu-id="a11d5-111">Lista wszystkich kontrolerów w ramach abonamentu.</span><span class="sxs-lookup"><span data-stu-id="a11d5-111">List all controllers in a subscription.</span></span>

### <span data-ttu-id="a11d5-112">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="a11d5-112">Example 2</span></span>
```powershell
PS C:\> Get-AzureRmDevSpacesController --ResourceGroupName devSpaceResourceGroup -Name devSpaceControllerName

Name        Resource Group  Location  Provisioning State
----------  --------------  --------  ------------------
devSpaceControllerName   devSpaceResourceGroup     eastus    Succeeded
```

<span data-ttu-id="a11d5-113">Uzyskaj kontrolery DevSpaces w ramach abonamentu.</span><span class="sxs-lookup"><span data-stu-id="a11d5-113">Get a DevSpaces controllers in a subscription.</span></span>

## <span data-ttu-id="a11d5-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="a11d5-114">PARAMETERS</span></span>

### <span data-ttu-id="a11d5-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a11d5-115">-DefaultProfile</span></span>
<span data-ttu-id="a11d5-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="a11d5-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a11d5-117">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="a11d5-117">-Name</span></span>
<span data-ttu-id="a11d5-118">Nazwa kontrolera DevSpaces.</span><span class="sxs-lookup"><span data-stu-id="a11d5-118">DevSpaces controller name.</span></span>

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

### <span data-ttu-id="a11d5-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a11d5-119">-ResourceGroupName</span></span>
<span data-ttu-id="a11d5-120">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="a11d5-120">Resource group name</span></span>

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

### <span data-ttu-id="a11d5-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a11d5-121">CommonParameters</span></span>
<span data-ttu-id="a11d5-122">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a11d5-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a11d5-123">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a11d5-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a11d5-124">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a11d5-124">INPUTS</span></span>

### <span data-ttu-id="a11d5-125">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="a11d5-125">None</span></span>

## <span data-ttu-id="a11d5-126">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="a11d5-126">OUTPUTS</span></span>

### <span data-ttu-id="a11d5-127">Microsoft. Azure. Commands. DevSpaces. models. PSController</span><span class="sxs-lookup"><span data-stu-id="a11d5-127">Microsoft.Azure.Commands.DevSpaces.Models.PSController</span></span>

## <span data-ttu-id="a11d5-128">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="a11d5-128">NOTES</span></span>

## <span data-ttu-id="a11d5-129">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="a11d5-129">RELATED LINKS</span></span>
