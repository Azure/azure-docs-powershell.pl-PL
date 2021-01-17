---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ContainerRegistry.dll-Help.xml
Module Name: Az.ContainerRegistry
online version: https://docs.microsoft.com/en-us/powershell/module/az.containerregistry/test-azcontainerregistrynameavailability
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Test-AzContainerRegistryNameAvailability.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Test-AzContainerRegistryNameAvailability.md
ms.openlocfilehash: 153ed152c68444327f379fda9ab5009290cbc00a
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98347518"
---
# <span data-ttu-id="23ce1-101">Test-AzContainerRegistryNameAvailability</span><span class="sxs-lookup"><span data-stu-id="23ce1-101">Test-AzContainerRegistryNameAvailability</span></span>

## <span data-ttu-id="23ce1-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="23ce1-102">SYNOPSIS</span></span>
<span data-ttu-id="23ce1-103">Sprawdza dostępność nazwy rejestru kontenera.</span><span class="sxs-lookup"><span data-stu-id="23ce1-103">Checks the availability of a container registry name.</span></span>

## <span data-ttu-id="23ce1-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="23ce1-104">SYNTAX</span></span>

```
Test-AzContainerRegistryNameAvailability [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="23ce1-105">Opis</span><span class="sxs-lookup"><span data-stu-id="23ce1-105">DESCRIPTION</span></span>
<span data-ttu-id="23ce1-106">Polecenie cmdlet Test-AzContainerRegistryNameAvailability sprawdza, czy nazwa rejestru kontenera jest prawidłowa i czy można z niej korzystać.</span><span class="sxs-lookup"><span data-stu-id="23ce1-106">The Test-AzContainerRegistryNameAvailability cmdlet checks whether a container registry name is valid and available to use.</span></span>

## <span data-ttu-id="23ce1-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="23ce1-107">EXAMPLES</span></span>

### <span data-ttu-id="23ce1-108">Przykład 1: sprawdza dostępność nazwy rejestru kontenera</span><span class="sxs-lookup"><span data-stu-id="23ce1-108">Example 1: Checks the availability of a container registry name</span></span>
```powershell
PS C:\>Test-AzContainerRegistryNameAvailability -Name 'SomeRegistryName'

NameAvailable Reason Message
------------- ------ -------
         True
```

<span data-ttu-id="23ce1-109">To polecenie sprawdza dostępność nazwy rejestru kontenera \` SomeRegistryName \` .</span><span class="sxs-lookup"><span data-stu-id="23ce1-109">This command checks the availability of the container registry name \`SomeRegistryName\`.</span></span>

## <span data-ttu-id="23ce1-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="23ce1-110">PARAMETERS</span></span>

### <span data-ttu-id="23ce1-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="23ce1-111">-DefaultProfile</span></span>
<span data-ttu-id="23ce1-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="23ce1-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="23ce1-113">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="23ce1-113">-Name</span></span>
<span data-ttu-id="23ce1-114">Nazwa rejestru kontenera.</span><span class="sxs-lookup"><span data-stu-id="23ce1-114">Container Registry Name.</span></span>

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

### <span data-ttu-id="23ce1-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="23ce1-115">CommonParameters</span></span>
<span data-ttu-id="23ce1-116">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="23ce1-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="23ce1-117">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="23ce1-117">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="23ce1-118">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="23ce1-118">INPUTS</span></span>

### <span data-ttu-id="23ce1-119">System. String</span><span class="sxs-lookup"><span data-stu-id="23ce1-119">System.String</span></span>

## <span data-ttu-id="23ce1-120">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="23ce1-120">OUTPUTS</span></span>

### <span data-ttu-id="23ce1-121">Microsoft. Azure. Management. ContainerRegistry. MODELES. RegistryNameStatus</span><span class="sxs-lookup"><span data-stu-id="23ce1-121">Microsoft.Azure.Management.ContainerRegistry.Models.RegistryNameStatus</span></span>

## <span data-ttu-id="23ce1-122">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="23ce1-122">NOTES</span></span>

## <span data-ttu-id="23ce1-123">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="23ce1-123">RELATED LINKS</span></span>

[<span data-ttu-id="23ce1-124">Nowe — AzContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="23ce1-124">New-AzContainerRegistry</span></span>]()

