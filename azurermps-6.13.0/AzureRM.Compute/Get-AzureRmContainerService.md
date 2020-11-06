---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: AFF75E0B-CB88-45ED-9067-7F43E2BA485C
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/get-azurermcontainerservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Get-AzureRmContainerService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Get-AzureRmContainerService.md
ms.openlocfilehash: 0f87254f72d0b5ac22a5770ad3f1a9d03b70fd34
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93541899"
---
# <span data-ttu-id="ba57c-101">Get-AzureRmContainerService</span><span class="sxs-lookup"><span data-stu-id="ba57c-101">Get-AzureRmContainerService</span></span>

## <span data-ttu-id="ba57c-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="ba57c-102">SYNOPSIS</span></span>
<span data-ttu-id="ba57c-103">Pobiera usługę kontenera.</span><span class="sxs-lookup"><span data-stu-id="ba57c-103">Gets a container service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ba57c-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="ba57c-104">SYNTAX</span></span>

```
Get-AzureRmContainerService [[-ResourceGroupName] <String>] [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ba57c-105">Opis</span><span class="sxs-lookup"><span data-stu-id="ba57c-105">DESCRIPTION</span></span>
<span data-ttu-id="ba57c-106">Polecenie cmdlet **Get-AzureRmContainerService** pobiera usługę kontenera.</span><span class="sxs-lookup"><span data-stu-id="ba57c-106">The **Get-AzureRmContainerService** cmdlet gets a container service.</span></span>
<span data-ttu-id="ba57c-107">Możesz wyświetlić właściwości usługi kontenera zawierającej stan, liczbę wzorców i agentów oraz w pełni kwalifikowaną nazwę domeny dla wzorców i agentów.</span><span class="sxs-lookup"><span data-stu-id="ba57c-107">You can view the properties of a container service, which include state, number of master and agents, and fully qualified domain name of master and agent.</span></span>

## <span data-ttu-id="ba57c-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="ba57c-108">EXAMPLES</span></span>

### <span data-ttu-id="ba57c-109">Przykład 1: Uzyskiwanie usługi kontenera</span><span class="sxs-lookup"><span data-stu-id="ba57c-109">Example 1: Get a container service</span></span>
```
PS C:\> Get-AzureRmContainerService -ResourceGroupName "ResourceGroup17" -Name "CSResourceGroup17"
```

<span data-ttu-id="ba57c-110">To polecenie uzyskuje usługę kontenera o nazwie CSResourceGroup17.</span><span class="sxs-lookup"><span data-stu-id="ba57c-110">This command gets a container service named CSResourceGroup17.</span></span>

## <span data-ttu-id="ba57c-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="ba57c-111">PARAMETERS</span></span>

### <span data-ttu-id="ba57c-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ba57c-112">-DefaultProfile</span></span>
<span data-ttu-id="ba57c-113">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="ba57c-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ba57c-114">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="ba57c-114">-Name</span></span>
<span data-ttu-id="ba57c-115">Określa nazwę usługi kontenera, która jest pobierana przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ba57c-115">Specifies the name of the container service that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ba57c-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ba57c-116">-ResourceGroupName</span></span>
<span data-ttu-id="ba57c-117">Określa grupę zasobów usługi kontenera, która jest pobierana przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ba57c-117">Specifies the resource group of the container service that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ba57c-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ba57c-118">CommonParameters</span></span>
<span data-ttu-id="ba57c-119">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ba57c-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ba57c-120">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ba57c-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ba57c-121">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ba57c-121">INPUTS</span></span>

### <span data-ttu-id="ba57c-122">System. String</span><span class="sxs-lookup"><span data-stu-id="ba57c-122">System.String</span></span>

## <span data-ttu-id="ba57c-123">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="ba57c-123">OUTPUTS</span></span>

### <span data-ttu-id="ba57c-124">Microsoft. Azure. Commands. COMPUTE. Automation. MODELES. PSContainerService</span><span class="sxs-lookup"><span data-stu-id="ba57c-124">Microsoft.Azure.Commands.Compute.Automation.Models.PSContainerService</span></span>

## <span data-ttu-id="ba57c-125">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="ba57c-125">NOTES</span></span>

## <span data-ttu-id="ba57c-126">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="ba57c-126">RELATED LINKS</span></span>

[<span data-ttu-id="ba57c-127">Nowe — AzureRmContainerService</span><span class="sxs-lookup"><span data-stu-id="ba57c-127">New-AzureRmContainerService</span></span>](./New-AzureRmContainerService.md)

[<span data-ttu-id="ba57c-128">Remove-AzureRmContainerService</span><span class="sxs-lookup"><span data-stu-id="ba57c-128">Remove-AzureRmContainerService</span></span>](./Remove-AzureRmContainerService.md)

[<span data-ttu-id="ba57c-129">Update-AzureRmContainerService</span><span class="sxs-lookup"><span data-stu-id="ba57c-129">Update-AzureRmContainerService</span></span>](./Update-AzureRmContainerService.md)


