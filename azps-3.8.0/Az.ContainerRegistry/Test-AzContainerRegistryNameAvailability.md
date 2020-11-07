---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ContainerRegistry.dll-Help.xml
Module Name: Az.ContainerRegistry
online version: https://docs.microsoft.com/en-us/powershell/module/az.containerregistry/test-azcontainerregistrynameavailability
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Test-AzContainerRegistryNameAvailability.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Test-AzContainerRegistryNameAvailability.md
ms.openlocfilehash: 153ed152c68444327f379fda9ab5009290cbc00a
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/21/2020
ms.locfileid: "93894814"
---
# <span data-ttu-id="4cbbe-101">Test-AzContainerRegistryNameAvailability</span><span class="sxs-lookup"><span data-stu-id="4cbbe-101">Test-AzContainerRegistryNameAvailability</span></span>

## <span data-ttu-id="4cbbe-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="4cbbe-102">SYNOPSIS</span></span>
<span data-ttu-id="4cbbe-103">Sprawdza dostępność nazwy rejestru kontenera.</span><span class="sxs-lookup"><span data-stu-id="4cbbe-103">Checks the availability of a container registry name.</span></span>

## <span data-ttu-id="4cbbe-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="4cbbe-104">SYNTAX</span></span>

```
Test-AzContainerRegistryNameAvailability [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="4cbbe-105">Opis</span><span class="sxs-lookup"><span data-stu-id="4cbbe-105">DESCRIPTION</span></span>
<span data-ttu-id="4cbbe-106">Polecenie cmdlet Test-AzContainerRegistryNameAvailability sprawdza, czy nazwa rejestru kontenera jest prawidłowa i czy można z niej korzystać.</span><span class="sxs-lookup"><span data-stu-id="4cbbe-106">The Test-AzContainerRegistryNameAvailability cmdlet checks whether a container registry name is valid and available to use.</span></span>

## <span data-ttu-id="4cbbe-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="4cbbe-107">EXAMPLES</span></span>

### <span data-ttu-id="4cbbe-108">Przykład 1: sprawdza dostępność nazwy rejestru kontenera</span><span class="sxs-lookup"><span data-stu-id="4cbbe-108">Example 1: Checks the availability of a container registry name</span></span>
```powershell
PS C:\>Test-AzContainerRegistryNameAvailability -Name 'SomeRegistryName'

NameAvailable Reason Message
------------- ------ -------
         True
```

<span data-ttu-id="4cbbe-109">To polecenie sprawdza dostępność nazwy rejestru kontenera \` SomeRegistryName \` .</span><span class="sxs-lookup"><span data-stu-id="4cbbe-109">This command checks the availability of the container registry name \`SomeRegistryName\`.</span></span>

## <span data-ttu-id="4cbbe-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="4cbbe-110">PARAMETERS</span></span>

### <span data-ttu-id="4cbbe-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4cbbe-111">-DefaultProfile</span></span>
<span data-ttu-id="4cbbe-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="4cbbe-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="4cbbe-113">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="4cbbe-113">-Name</span></span>
<span data-ttu-id="4cbbe-114">Nazwa rejestru kontenera.</span><span class="sxs-lookup"><span data-stu-id="4cbbe-114">Container Registry Name.</span></span>

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

### <span data-ttu-id="4cbbe-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4cbbe-115">CommonParameters</span></span>
<span data-ttu-id="4cbbe-116">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4cbbe-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4cbbe-117">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="4cbbe-117">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4cbbe-118">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="4cbbe-118">INPUTS</span></span>

### <span data-ttu-id="4cbbe-119">System. String</span><span class="sxs-lookup"><span data-stu-id="4cbbe-119">System.String</span></span>

## <span data-ttu-id="4cbbe-120">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="4cbbe-120">OUTPUTS</span></span>

### <span data-ttu-id="4cbbe-121">Microsoft. Azure. Management. ContainerRegistry. MODELES. RegistryNameStatus</span><span class="sxs-lookup"><span data-stu-id="4cbbe-121">Microsoft.Azure.Management.ContainerRegistry.Models.RegistryNameStatus</span></span>

## <span data-ttu-id="4cbbe-122">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="4cbbe-122">NOTES</span></span>

## <span data-ttu-id="4cbbe-123">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="4cbbe-123">RELATED LINKS</span></span>

[<span data-ttu-id="4cbbe-124">Nowe — AzContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="4cbbe-124">New-AzContainerRegistry</span></span>]()

