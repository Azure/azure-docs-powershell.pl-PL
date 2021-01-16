---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ContainerRegistry.dll-Help.xml
Module Name: Az.ContainerRegistry
online version: https://docs.microsoft.com/en-us/powershell/module/az.containerregistry/get-azcontainerregistryusage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Get-AzContainerRegistryUsage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Get-AzContainerRegistryUsage.md
ms.openlocfilehash: e7d84439b2292d70604f3f7d9e827a0d8cc035e5
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98331321"
---
# <span data-ttu-id="4af97-101">Get-AzContainerRegistryUsage</span><span class="sxs-lookup"><span data-stu-id="4af97-101">Get-AzContainerRegistryUsage</span></span>

## <span data-ttu-id="4af97-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="4af97-102">SYNOPSIS</span></span>
<span data-ttu-id="4af97-103">Uzyskiwanie użycia rejestru kontenera platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="4af97-103">Get Usage of an azure container registry.</span></span>

## <span data-ttu-id="4af97-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="4af97-104">SYNTAX</span></span>

```
Get-AzContainerRegistryUsage -ResourceGroupName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4af97-105">Opis</span><span class="sxs-lookup"><span data-stu-id="4af97-105">DESCRIPTION</span></span>
<span data-ttu-id="4af97-106">Uzyskiwanie użycia rejestru kontenera platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="4af97-106">Get Usage of an azure container registry.</span></span>

## <span data-ttu-id="4af97-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="4af97-107">EXAMPLES</span></span>

### <span data-ttu-id="4af97-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="4af97-108">Example 1</span></span>
```powershell
PS C:\> Get-AzContainerRegistryUsage -ResourceGroupName $resourceGroupName -RegistryName $RegistryName
```

<span data-ttu-id="4af97-109">Uzyskiwanie użycia rejestru kontenera platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="4af97-109">Get Usage of an azure container registry.</span></span>

## <span data-ttu-id="4af97-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="4af97-110">PARAMETERS</span></span>

### <span data-ttu-id="4af97-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4af97-111">-DefaultProfile</span></span>
<span data-ttu-id="4af97-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="4af97-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4af97-113">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="4af97-113">-Name</span></span>
<span data-ttu-id="4af97-114">Nazwa rejestru docelowego.</span><span class="sxs-lookup"><span data-stu-id="4af97-114">Target registry name.</span></span>

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

### <span data-ttu-id="4af97-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4af97-115">-ResourceGroupName</span></span>
<span data-ttu-id="4af97-116">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="4af97-116">Resource group name.</span></span>

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

### <span data-ttu-id="4af97-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4af97-117">CommonParameters</span></span>
<span data-ttu-id="4af97-118">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4af97-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4af97-119">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="4af97-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4af97-120">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="4af97-120">INPUTS</span></span>

### <span data-ttu-id="4af97-121">System. String</span><span class="sxs-lookup"><span data-stu-id="4af97-121">System.String</span></span>

## <span data-ttu-id="4af97-122">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="4af97-122">OUTPUTS</span></span>

### <span data-ttu-id="4af97-123">Microsoft. Azure. Commands. ContainerRegistry. models. PSRegistryUsage</span><span class="sxs-lookup"><span data-stu-id="4af97-123">Microsoft.Azure.Commands.ContainerRegistry.Models.PSRegistryUsage</span></span>

## <span data-ttu-id="4af97-124">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="4af97-124">NOTES</span></span>

## <span data-ttu-id="4af97-125">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="4af97-125">RELATED LINKS</span></span>
