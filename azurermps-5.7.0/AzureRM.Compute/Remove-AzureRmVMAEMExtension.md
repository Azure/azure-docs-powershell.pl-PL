---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: B1CD5302-9BF0-460E-98FE-F60DFE072848
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRmVMAEMExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRmVMAEMExtension.md
ms.openlocfilehash: fb31bffbdb61c42ea1388c85b71f26af69056c54
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93544479"
---
# <span data-ttu-id="c0703-101">Remove-AzureRmVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="c0703-101">Remove-AzureRmVMAEMExtension</span></span>

## <span data-ttu-id="c0703-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="c0703-102">SYNOPSIS</span></span>
<span data-ttu-id="c0703-103">Usuwa rozszerzenie AEM z maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="c0703-103">Removes the AEM extension from a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c0703-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="c0703-104">SYNTAX</span></span>

```
Remove-AzureRmVMAEMExtension [-ResourceGroupName] <String> [-VMName] <String> [[-Name] <String>]
 [[-OSType] <String>] [<CommonParameters>]
```

## <span data-ttu-id="c0703-105">Opis</span><span class="sxs-lookup"><span data-stu-id="c0703-105">DESCRIPTION</span></span>
<span data-ttu-id="c0703-106">Polecenie cmdlet **Remove-AzureRmVMAEMExtension** usuwa rozszerzenie rozszerzonego monitorowania platformy Azure (AEM) z maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="c0703-106">The **Remove-AzureRmVMAEMExtension** cmdlet removes the Azure Enhanced Monitoring (AEM) extension from a virtual machine.</span></span>

## <span data-ttu-id="c0703-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="c0703-107">EXAMPLES</span></span>

### <span data-ttu-id="c0703-108">Przykład 1. Usuń rozszerzenie AEM</span><span class="sxs-lookup"><span data-stu-id="c0703-108">Example 1: Remove the AEM extension</span></span>
```
PS C:\> Remove-AzureRmVMAEMExtension -ResourceGroupName "ResourceGroup11" -VMName "contoso-server"
```

<span data-ttu-id="c0703-109">To polecenie usuwa rozszerzenie AEM dla maszyny wirtualnej o nazwie contoso — serwer.</span><span class="sxs-lookup"><span data-stu-id="c0703-109">This command removes the AEM extension for the virtual machine named contoso-server.</span></span>

## <span data-ttu-id="c0703-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="c0703-110">PARAMETERS</span></span>

### <span data-ttu-id="c0703-111">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="c0703-111">-Name</span></span>
<span data-ttu-id="c0703-112">Określa nazwę maszyny wirtualnej, z której to polecenie cmdlet usuwa rozszerzenie AEM.</span><span class="sxs-lookup"><span data-stu-id="c0703-112">Specifies the name of the virtual machine from which this cmdlet removes the AEM extension.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ExtensionName

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c0703-113">-OSType</span><span class="sxs-lookup"><span data-stu-id="c0703-113">-OSType</span></span>
<span data-ttu-id="c0703-114">Określa typ systemu operacyjnego dysku systemu operacyjnego.</span><span class="sxs-lookup"><span data-stu-id="c0703-114">Specifies the type of the operating system of the operating system disk.</span></span>
<span data-ttu-id="c0703-115">Jeśli dysk systemu operacyjnego nie ma typu, należy określić ten parametr.</span><span class="sxs-lookup"><span data-stu-id="c0703-115">If the operating system disk does not have a type, you must specify this parameter.</span></span>
<span data-ttu-id="c0703-116">Dopuszczalne wartości tego parametru to: Windows i Linux.</span><span class="sxs-lookup"><span data-stu-id="c0703-116">The acceptable values for this parameter are: Windows and Linux.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c0703-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c0703-117">-ResourceGroupName</span></span>
<span data-ttu-id="c0703-118">Określa nazwę grupy zasobów maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="c0703-118">Specifies the name of the resource group of a virtual machine.</span></span>
<span data-ttu-id="c0703-119">To polecenie cmdlet usuwa rozszerzenie AEM z tej maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="c0703-119">This cmdlet removes the AEM extension from that virtual machine.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c0703-120">-VMName</span><span class="sxs-lookup"><span data-stu-id="c0703-120">-VMName</span></span>
<span data-ttu-id="c0703-121">Określa nazwę maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="c0703-121">Specifies the name of a virtual machine.</span></span>
<span data-ttu-id="c0703-122">To polecenie cmdlet usuwa rozszerzenie AEM dla maszyny wirtualnej, którą określa ten parametr.</span><span class="sxs-lookup"><span data-stu-id="c0703-122">This cmdlet removes the AEM extension for the virtual machine that this parameter specifies.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c0703-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c0703-123">CommonParameters</span></span>
<span data-ttu-id="c0703-124">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c0703-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c0703-125">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c0703-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c0703-126">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="c0703-126">INPUTS</span></span>

### <span data-ttu-id="c0703-127">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="c0703-127">None</span></span>
<span data-ttu-id="c0703-128">To polecenie cmdlet nie akceptuje żadnych danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="c0703-128">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="c0703-129">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="c0703-129">OUTPUTS</span></span>

## <span data-ttu-id="c0703-130">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="c0703-130">NOTES</span></span>

## <span data-ttu-id="c0703-131">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="c0703-131">RELATED LINKS</span></span>

[<span data-ttu-id="c0703-132">Get-AzureRmVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="c0703-132">Get-AzureRmVMAEMExtension</span></span>](./Get-AzureRmVMAEMExtension.md)

[<span data-ttu-id="c0703-133">Set-AzureRmVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="c0703-133">Set-AzureRmVMAEMExtension</span></span>](./Set-AzureRmVMAEMExtension.md)

[<span data-ttu-id="c0703-134">Test — AzureRmVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="c0703-134">Test-AzureRmVMAEMExtension</span></span>](./Test-AzureRmVMAEMExtension.md)


