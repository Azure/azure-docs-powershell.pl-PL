---
external help file: Microsoft.Azure.Commands.ContainerRegistry.dll-Help.xml
Module Name: AzureRM.ContainerRegistry
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.containerregistry/test-azurermcontainerregistrynameavailability
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerRegistry/Commands.ContainerRegistry/help/Test-AzureRmContainerRegistryNameAvailability.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerRegistry/Commands.ContainerRegistry/help/Test-AzureRmContainerRegistryNameAvailability.md
ms.openlocfilehash: da415c21532ea0b2178cc2a75d6a3d09bdc2d50b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93546816"
---
# <span data-ttu-id="5c544-101">Test-AzureRmContainerRegistryNameAvailability</span><span class="sxs-lookup"><span data-stu-id="5c544-101">Test-AzureRmContainerRegistryNameAvailability</span></span>

## <span data-ttu-id="5c544-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="5c544-102">SYNOPSIS</span></span>
<span data-ttu-id="5c544-103">Sprawdza dostępność nazwy rejestru kontenera.</span><span class="sxs-lookup"><span data-stu-id="5c544-103">Checks the availability of a container registry name.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5c544-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="5c544-104">SYNTAX</span></span>

```
Test-AzureRmContainerRegistryNameAvailability [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="5c544-105">Opis</span><span class="sxs-lookup"><span data-stu-id="5c544-105">DESCRIPTION</span></span>
<span data-ttu-id="5c544-106">Polecenie cmdlet Test-AzureRmContainerRegistryNameAvailability sprawdza, czy nazwa rejestru kontenera jest prawidłowa i czy można z niej korzystać.</span><span class="sxs-lookup"><span data-stu-id="5c544-106">The Test-AzureRmContainerRegistryNameAvailability cmdlet checks whether a container registry name is valid and available to use.</span></span>

## <span data-ttu-id="5c544-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="5c544-107">EXAMPLES</span></span>

### <span data-ttu-id="5c544-108">Przykład 1: sprawdza dostępność nazwy rejestru kontenera</span><span class="sxs-lookup"><span data-stu-id="5c544-108">Example 1: Checks the availability of a container registry name</span></span>
```powershell
PS C:\>Test-AzureRmContainerRegistryNameAvailability -Name 'SomeRegistryName'

NameAvailable Reason Message
------------- ------ -------
         True
```

<span data-ttu-id="5c544-109">To polecenie sprawdza dostępność nazwy rejestru kontenera \` SomeRegistryName \` .</span><span class="sxs-lookup"><span data-stu-id="5c544-109">This command checks the availability of the container registry name \`SomeRegistryName\`.</span></span>

## <span data-ttu-id="5c544-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="5c544-110">PARAMETERS</span></span>

### <span data-ttu-id="5c544-111">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="5c544-111">-Name</span></span>
<span data-ttu-id="5c544-112">Nazwa rejestru kontenera.</span><span class="sxs-lookup"><span data-stu-id="5c544-112">Container Registry Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ContainerRegistryName, RegistryName, ResourceName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5c544-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5c544-113">-DefaultProfile</span></span>
<span data-ttu-id="5c544-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="5c544-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5c544-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5c544-115">CommonParameters</span></span>
<span data-ttu-id="5c544-116">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5c544-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5c544-117">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5c544-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5c544-118">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="5c544-118">INPUTS</span></span>

### <span data-ttu-id="5c544-119">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="5c544-119">None</span></span>
<span data-ttu-id="5c544-120">To polecenie cmdlet nie akceptuje żadnych danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="5c544-120">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="5c544-121">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="5c544-121">OUTPUTS</span></span>

### <span data-ttu-id="5c544-122">Microsoft. Azure. Management. ContainerRegistry. MODELES. RegistryNameStatus</span><span class="sxs-lookup"><span data-stu-id="5c544-122">Microsoft.Azure.Management.ContainerRegistry.Models.RegistryNameStatus</span></span>

## <span data-ttu-id="5c544-123">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="5c544-123">NOTES</span></span>

## <span data-ttu-id="5c544-124">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="5c544-124">RELATED LINKS</span></span>

[<span data-ttu-id="5c544-125">Nowe — AzureRmContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="5c544-125">New-AzureRmContainerRegistry</span></span>]()

