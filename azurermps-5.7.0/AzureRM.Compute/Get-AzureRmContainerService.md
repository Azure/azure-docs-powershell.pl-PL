---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: AFF75E0B-CB88-45ED-9067-7F43E2BA485C
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmContainerService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmContainerService.md
ms.openlocfilehash: d2a53d221adf7483899056791aefd00b03aca26e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93546895"
---
# <span data-ttu-id="be382-101">Get-AzureRmContainerService</span><span class="sxs-lookup"><span data-stu-id="be382-101">Get-AzureRmContainerService</span></span>

## <span data-ttu-id="be382-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="be382-102">SYNOPSIS</span></span>
<span data-ttu-id="be382-103">Pobiera usługę kontenera.</span><span class="sxs-lookup"><span data-stu-id="be382-103">Gets a container service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="be382-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="be382-104">SYNTAX</span></span>

```
Get-AzureRmContainerService [[-ResourceGroupName] <String>] [[-Name] <String>] [<CommonParameters>]
```

## <span data-ttu-id="be382-105">Opis</span><span class="sxs-lookup"><span data-stu-id="be382-105">DESCRIPTION</span></span>
<span data-ttu-id="be382-106">Polecenie cmdlet **Get-AzureRmContainerService** pobiera usługę kontenera.</span><span class="sxs-lookup"><span data-stu-id="be382-106">The **Get-AzureRmContainerService** cmdlet gets a container service.</span></span>
<span data-ttu-id="be382-107">Możesz wyświetlić właściwości usługi kontenera zawierającej stan, liczbę wzorców i agentów oraz w pełni kwalifikowaną nazwę domeny dla wzorców i agentów.</span><span class="sxs-lookup"><span data-stu-id="be382-107">You can view the properties of a container service, which include state, number of master and agents, and fully qualified domain name of master and agent.</span></span>

## <span data-ttu-id="be382-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="be382-108">EXAMPLES</span></span>

### <span data-ttu-id="be382-109">Przykład 1: Uzyskiwanie usługi kontenera</span><span class="sxs-lookup"><span data-stu-id="be382-109">Example 1: Get a container service</span></span>
```
PS C:\> Get-AzureRmContainerService -ResourceGroupName "ResourceGroup17" -Name "CSResourceGroup17"
```

<span data-ttu-id="be382-110">To polecenie uzyskuje usługę kontenera o nazwie CSResourceGroup17.</span><span class="sxs-lookup"><span data-stu-id="be382-110">This command gets a container service named CSResourceGroup17.</span></span>

## <span data-ttu-id="be382-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="be382-111">PARAMETERS</span></span>

### <span data-ttu-id="be382-112">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="be382-112">-Name</span></span>
<span data-ttu-id="be382-113">Określa nazwę usługi kontenera, która jest pobierana przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="be382-113">Specifies the name of the container service that this cmdlet gets.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="be382-114">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="be382-114">-ResourceGroupName</span></span>
<span data-ttu-id="be382-115">Określa grupę zasobów usługi kontenera, która jest pobierana przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="be382-115">Specifies the resource group of the container service that this cmdlet gets.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="be382-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="be382-116">CommonParameters</span></span>
<span data-ttu-id="be382-117">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="be382-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="be382-118">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="be382-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="be382-119">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="be382-119">INPUTS</span></span>

### <span data-ttu-id="be382-120">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="be382-120">None</span></span>
<span data-ttu-id="be382-121">To polecenie cmdlet nie akceptuje żadnych danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="be382-121">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="be382-122">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="be382-122">OUTPUTS</span></span>

## <span data-ttu-id="be382-123">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="be382-123">NOTES</span></span>

## <span data-ttu-id="be382-124">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="be382-124">RELATED LINKS</span></span>

[<span data-ttu-id="be382-125">Nowe — AzureRmContainerService</span><span class="sxs-lookup"><span data-stu-id="be382-125">New-AzureRmContainerService</span></span>](./New-AzureRmContainerService.md)

[<span data-ttu-id="be382-126">Remove-AzureRmContainerService</span><span class="sxs-lookup"><span data-stu-id="be382-126">Remove-AzureRmContainerService</span></span>](./Remove-AzureRmContainerService.md)

[<span data-ttu-id="be382-127">Update-AzureRmContainerService</span><span class="sxs-lookup"><span data-stu-id="be382-127">Update-AzureRmContainerService</span></span>](./Update-AzureRmContainerService.md)


