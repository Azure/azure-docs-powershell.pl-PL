---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ContainerRegistry.dll-Help.xml
Module Name: Az.ContainerRegistry
online version: https://docs.microsoft.com/powershell/module/az.containerregistry/get-azcontainerregistryusage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Get-AzContainerRegistryUsage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Get-AzContainerRegistryUsage.md
ms.openlocfilehash: 7a950bc3b375ea9d86ef71eda120ac1d92fbd8e9
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101990347"
---
# <span data-ttu-id="ea954-101">Get-AzContainerRegistryUsage</span><span class="sxs-lookup"><span data-stu-id="ea954-101">Get-AzContainerRegistryUsage</span></span>

## <span data-ttu-id="ea954-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ea954-102">SYNOPSIS</span></span>
<span data-ttu-id="ea954-103">Pobierz użycie rejestru azure container.</span><span class="sxs-lookup"><span data-stu-id="ea954-103">Get Usage of an azure container registry.</span></span>

## <span data-ttu-id="ea954-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="ea954-104">SYNTAX</span></span>

```
Get-AzContainerRegistryUsage -ResourceGroupName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ea954-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="ea954-105">DESCRIPTION</span></span>
<span data-ttu-id="ea954-106">Pobierz użycie rejestru azure container.</span><span class="sxs-lookup"><span data-stu-id="ea954-106">Get Usage of an azure container registry.</span></span>

## <span data-ttu-id="ea954-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="ea954-107">EXAMPLES</span></span>

### <span data-ttu-id="ea954-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="ea954-108">Example 1</span></span>
```powershell
PS C:\> Get-AzContainerRegistryUsage -ResourceGroupName $resourceGroupName -RegistryName $RegistryName
```

<span data-ttu-id="ea954-109">Pobierz użycie rejestru azure container.</span><span class="sxs-lookup"><span data-stu-id="ea954-109">Get Usage of an azure container registry.</span></span>

## <span data-ttu-id="ea954-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ea954-110">PARAMETERS</span></span>

### <span data-ttu-id="ea954-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ea954-111">-DefaultProfile</span></span>
<span data-ttu-id="ea954-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="ea954-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ea954-113">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="ea954-113">-Name</span></span>
<span data-ttu-id="ea954-114">Docelowa nazwa rejestru.</span><span class="sxs-lookup"><span data-stu-id="ea954-114">Target registry name.</span></span>

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

### <span data-ttu-id="ea954-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ea954-115">-ResourceGroupName</span></span>
<span data-ttu-id="ea954-116">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="ea954-116">Resource group name.</span></span>

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

### <span data-ttu-id="ea954-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ea954-117">CommonParameters</span></span>
<span data-ttu-id="ea954-118">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ea954-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ea954-119">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="ea954-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ea954-120">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ea954-120">INPUTS</span></span>

### <span data-ttu-id="ea954-121">System.String</span><span class="sxs-lookup"><span data-stu-id="ea954-121">System.String</span></span>

## <span data-ttu-id="ea954-122">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ea954-122">OUTPUTS</span></span>

### <span data-ttu-id="ea954-123">Microsoft.Azure.Commands.ContainerRegistry.Models.PSRegistryUsage</span><span class="sxs-lookup"><span data-stu-id="ea954-123">Microsoft.Azure.Commands.ContainerRegistry.Models.PSRegistryUsage</span></span>

## <span data-ttu-id="ea954-124">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="ea954-124">NOTES</span></span>

## <span data-ttu-id="ea954-125">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="ea954-125">RELATED LINKS</span></span>
