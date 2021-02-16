---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ContainerRegistry.dll-Help.xml
Module Name: Az.ContainerRegistry
online version: https://docs.microsoft.com/en-us/powershell/module/az.containerregistry/test-azcontainerregistrynameavailability
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Test-AzContainerRegistryNameAvailability.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Test-AzContainerRegistryNameAvailability.md
ms.openlocfilehash: 153ed152c68444327f379fda9ab5009290cbc00a
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100199091"
---
# <span data-ttu-id="81f9d-101">Test-AzContainerRegistryNameAvailability</span><span class="sxs-lookup"><span data-stu-id="81f9d-101">Test-AzContainerRegistryNameAvailability</span></span>

## <span data-ttu-id="81f9d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="81f9d-102">SYNOPSIS</span></span>
<span data-ttu-id="81f9d-103">Sprawdza dostępność nazwy rejestru kontenera.</span><span class="sxs-lookup"><span data-stu-id="81f9d-103">Checks the availability of a container registry name.</span></span>

## <span data-ttu-id="81f9d-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="81f9d-104">SYNTAX</span></span>

```
Test-AzContainerRegistryNameAvailability [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="81f9d-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="81f9d-105">DESCRIPTION</span></span>
<span data-ttu-id="81f9d-106">Polecenie Test-AzContainerRegistryNameAvailability sprawdza, czy nazwa rejestru kontenera jest prawidłowa i dostępna do użycia.</span><span class="sxs-lookup"><span data-stu-id="81f9d-106">The Test-AzContainerRegistryNameAvailability cmdlet checks whether a container registry name is valid and available to use.</span></span>

## <span data-ttu-id="81f9d-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="81f9d-107">EXAMPLES</span></span>

### <span data-ttu-id="81f9d-108">Przykład 1. Sprawdza dostępność nazwy rejestru kontenera</span><span class="sxs-lookup"><span data-stu-id="81f9d-108">Example 1: Checks the availability of a container registry name</span></span>
```powershell
PS C:\>Test-AzContainerRegistryNameAvailability -Name 'SomeRegistryName'

NameAvailable Reason Message
------------- ------ -------
         True
```

<span data-ttu-id="81f9d-109">To polecenie sprawdza dostępność nazwy rejestru kontenera \` NazwaRegistry. \`</span><span class="sxs-lookup"><span data-stu-id="81f9d-109">This command checks the availability of the container registry name \`SomeRegistryName\`.</span></span>

## <span data-ttu-id="81f9d-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="81f9d-110">PARAMETERS</span></span>

### <span data-ttu-id="81f9d-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="81f9d-111">-DefaultProfile</span></span>
<span data-ttu-id="81f9d-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="81f9d-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="81f9d-113">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="81f9d-113">-Name</span></span>
<span data-ttu-id="81f9d-114">Container Registry Name (Nazwa rejestru kontenera).</span><span class="sxs-lookup"><span data-stu-id="81f9d-114">Container Registry Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ContainerRegistryName, RegistryName, ResourceName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="81f9d-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="81f9d-115">CommonParameters</span></span>
<span data-ttu-id="81f9d-116">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="81f9d-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="81f9d-117">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="81f9d-117">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="81f9d-118">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="81f9d-118">INPUTS</span></span>

### <span data-ttu-id="81f9d-119">System.String</span><span class="sxs-lookup"><span data-stu-id="81f9d-119">System.String</span></span>

## <span data-ttu-id="81f9d-120">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="81f9d-120">OUTPUTS</span></span>

### <span data-ttu-id="81f9d-121">Microsoft.Azure.Management.ContainerRegistry.Models.RegistryNameStatus</span><span class="sxs-lookup"><span data-stu-id="81f9d-121">Microsoft.Azure.Management.ContainerRegistry.Models.RegistryNameStatus</span></span>

## <span data-ttu-id="81f9d-122">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="81f9d-122">NOTES</span></span>

## <span data-ttu-id="81f9d-123">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="81f9d-123">RELATED LINKS</span></span>

[<span data-ttu-id="81f9d-124">New-AzContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="81f9d-124">New-AzContainerRegistry</span></span>]()

