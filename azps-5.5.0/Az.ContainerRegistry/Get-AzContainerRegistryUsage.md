---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ContainerRegistry.dll-Help.xml
Module Name: Az.ContainerRegistry
online version: https://docs.microsoft.com/en-us/powershell/module/az.containerregistry/get-azcontainerregistryusage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Get-AzContainerRegistryUsage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Get-AzContainerRegistryUsage.md
ms.openlocfilehash: e7d84439b2292d70604f3f7d9e827a0d8cc035e5
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100181474"
---
# <span data-ttu-id="8a00e-101">Get-AzContainerRegistryUsage</span><span class="sxs-lookup"><span data-stu-id="8a00e-101">Get-AzContainerRegistryUsage</span></span>

## <span data-ttu-id="8a00e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8a00e-102">SYNOPSIS</span></span>
<span data-ttu-id="8a00e-103">Pobierz użycie rejestru azure container.</span><span class="sxs-lookup"><span data-stu-id="8a00e-103">Get Usage of an azure container registry.</span></span>

## <span data-ttu-id="8a00e-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="8a00e-104">SYNTAX</span></span>

```
Get-AzContainerRegistryUsage -ResourceGroupName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8a00e-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="8a00e-105">DESCRIPTION</span></span>
<span data-ttu-id="8a00e-106">Pobierz użycie rejestru azure container.</span><span class="sxs-lookup"><span data-stu-id="8a00e-106">Get Usage of an azure container registry.</span></span>

## <span data-ttu-id="8a00e-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="8a00e-107">EXAMPLES</span></span>

### <span data-ttu-id="8a00e-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="8a00e-108">Example 1</span></span>
```powershell
PS C:\> Get-AzContainerRegistryUsage -ResourceGroupName $resourceGroupName -RegistryName $RegistryName
```

<span data-ttu-id="8a00e-109">Pobierz użycie rejestru azure container.</span><span class="sxs-lookup"><span data-stu-id="8a00e-109">Get Usage of an azure container registry.</span></span>

## <span data-ttu-id="8a00e-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8a00e-110">PARAMETERS</span></span>

### <span data-ttu-id="8a00e-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8a00e-111">-DefaultProfile</span></span>
<span data-ttu-id="8a00e-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="8a00e-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8a00e-113">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="8a00e-113">-Name</span></span>
<span data-ttu-id="8a00e-114">Docelowa nazwa rejestru.</span><span class="sxs-lookup"><span data-stu-id="8a00e-114">Target registry name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: RegistryName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8a00e-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8a00e-115">-ResourceGroupName</span></span>
<span data-ttu-id="8a00e-116">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="8a00e-116">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8a00e-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8a00e-117">CommonParameters</span></span>
<span data-ttu-id="8a00e-118">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8a00e-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8a00e-119">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="8a00e-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8a00e-120">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="8a00e-120">INPUTS</span></span>

### <span data-ttu-id="8a00e-121">System.String</span><span class="sxs-lookup"><span data-stu-id="8a00e-121">System.String</span></span>

## <span data-ttu-id="8a00e-122">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="8a00e-122">OUTPUTS</span></span>

### <span data-ttu-id="8a00e-123">Microsoft.Azure.Commands.ContainerRegistry.Models.PSRegistryUsage</span><span class="sxs-lookup"><span data-stu-id="8a00e-123">Microsoft.Azure.Commands.ContainerRegistry.Models.PSRegistryUsage</span></span>

## <span data-ttu-id="8a00e-124">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="8a00e-124">NOTES</span></span>

## <span data-ttu-id="8a00e-125">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="8a00e-125">RELATED LINKS</span></span>
