---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
ms.assetid: AFF75E0B-CB88-45ED-9067-7F43E2BA485C
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azcontainerservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Get-AzContainerService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Get-AzContainerService.md
ms.openlocfilehash: 1a0daa4bf336ba970c12c24db3d5aab73641aaea
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/16/2020
ms.locfileid: "93893818"
---
# <span data-ttu-id="71c06-101">Get-AzContainerService</span><span class="sxs-lookup"><span data-stu-id="71c06-101">Get-AzContainerService</span></span>

## <span data-ttu-id="71c06-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="71c06-102">SYNOPSIS</span></span>
<span data-ttu-id="71c06-103">Pobiera usługę kontenera.</span><span class="sxs-lookup"><span data-stu-id="71c06-103">Gets a container service.</span></span>

## <span data-ttu-id="71c06-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="71c06-104">SYNTAX</span></span>

```
Get-AzContainerService [[-ResourceGroupName] <String>] [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="71c06-105">Opis</span><span class="sxs-lookup"><span data-stu-id="71c06-105">DESCRIPTION</span></span>
<span data-ttu-id="71c06-106">Polecenie cmdlet **Get-AzContainerService** pobiera usługę kontenera.</span><span class="sxs-lookup"><span data-stu-id="71c06-106">The **Get-AzContainerService** cmdlet gets a container service.</span></span>
<span data-ttu-id="71c06-107">Możesz wyświetlić właściwości usługi kontenera zawierającej stan, liczbę wzorców i agentów oraz w pełni kwalifikowaną nazwę domeny dla wzorców i agentów.</span><span class="sxs-lookup"><span data-stu-id="71c06-107">You can view the properties of a container service, which include state, number of master and agents, and fully qualified domain name of master and agent.</span></span>

## <span data-ttu-id="71c06-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="71c06-108">EXAMPLES</span></span>

### <span data-ttu-id="71c06-109">Przykład 1: Uzyskiwanie usługi kontenera</span><span class="sxs-lookup"><span data-stu-id="71c06-109">Example 1: Get a container service</span></span>
```
PS C:\> Get-AzContainerService -ResourceGroupName "ResourceGroup17" -Name "CSResourceGroup17"
```

<span data-ttu-id="71c06-110">To polecenie uzyskuje usługę kontenera o nazwie CSResourceGroup17.</span><span class="sxs-lookup"><span data-stu-id="71c06-110">This command gets a container service named CSResourceGroup17.</span></span>

## <span data-ttu-id="71c06-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="71c06-111">PARAMETERS</span></span>

### <span data-ttu-id="71c06-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="71c06-112">-DefaultProfile</span></span>
<span data-ttu-id="71c06-113">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="71c06-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="71c06-114">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="71c06-114">-Name</span></span>
<span data-ttu-id="71c06-115">Określa nazwę usługi kontenera, która jest pobierana przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="71c06-115">Specifies the name of the container service that this cmdlet gets.</span></span>

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

### <span data-ttu-id="71c06-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="71c06-116">-ResourceGroupName</span></span>
<span data-ttu-id="71c06-117">Określa grupę zasobów usługi kontenera, która jest pobierana przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="71c06-117">Specifies the resource group of the container service that this cmdlet gets.</span></span>

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

### <span data-ttu-id="71c06-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="71c06-118">CommonParameters</span></span>
<span data-ttu-id="71c06-119">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="71c06-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="71c06-120">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="71c06-120">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="71c06-121">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="71c06-121">INPUTS</span></span>

### <span data-ttu-id="71c06-122">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="71c06-122">None</span></span>
<span data-ttu-id="71c06-123">To polecenie cmdlet nie akceptuje żadnych danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="71c06-123">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="71c06-124">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="71c06-124">OUTPUTS</span></span>

### <span data-ttu-id="71c06-125">Microsoft. Azure. Commands. COMPUTE. Automation. MODELES. PSContainerService</span><span class="sxs-lookup"><span data-stu-id="71c06-125">Microsoft.Azure.Commands.Compute.Automation.Models.PSContainerService</span></span>

## <span data-ttu-id="71c06-126">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="71c06-126">NOTES</span></span>

## <span data-ttu-id="71c06-127">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="71c06-127">RELATED LINKS</span></span>

[<span data-ttu-id="71c06-128">Nowe — AzContainerService</span><span class="sxs-lookup"><span data-stu-id="71c06-128">New-AzContainerService</span></span>](./New-AzContainerService.md)

[<span data-ttu-id="71c06-129">Remove-AzContainerService</span><span class="sxs-lookup"><span data-stu-id="71c06-129">Remove-AzContainerService</span></span>](./Remove-AzContainerService.md)

[<span data-ttu-id="71c06-130">Update-AzContainerService</span><span class="sxs-lookup"><span data-stu-id="71c06-130">Update-AzContainerService</span></span>](./Update-AzContainerService.md)


