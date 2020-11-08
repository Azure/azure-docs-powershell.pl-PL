---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: B1CD5302-9BF0-460E-98FE-F60DFE072848
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azvmaemextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVMAEMExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVMAEMExtension.md
ms.openlocfilehash: 6ed6176b0f30a754156d2ce03ed0d5acad6e48f0
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/21/2020
ms.locfileid: "94051082"
---
# <span data-ttu-id="72d27-101">Remove-AzVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="72d27-101">Remove-AzVMAEMExtension</span></span>

## <span data-ttu-id="72d27-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="72d27-102">SYNOPSIS</span></span>
<span data-ttu-id="72d27-103">Usuwa rozszerzenie AEM z maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="72d27-103">Removes the AEM extension from a virtual machine.</span></span>

## <span data-ttu-id="72d27-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="72d27-104">SYNTAX</span></span>

```
Remove-AzVMAEMExtension [-ResourceGroupName] <String> [-VMName] <String> [[-Name] <String>]
 [[-OSType] <String>] [-NoWait] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="72d27-105">Opis</span><span class="sxs-lookup"><span data-stu-id="72d27-105">DESCRIPTION</span></span>
<span data-ttu-id="72d27-106">Polecenie cmdlet **Remove-AzVMAEMExtension** usuwa rozszerzenie rozszerzonego monitorowania platformy Azure (AEM) z maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="72d27-106">The **Remove-AzVMAEMExtension** cmdlet removes the Azure Enhanced Monitoring (AEM) extension from a virtual machine.</span></span>

## <span data-ttu-id="72d27-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="72d27-107">EXAMPLES</span></span>

### <span data-ttu-id="72d27-108">Przykład 1. Usuń rozszerzenie AEM</span><span class="sxs-lookup"><span data-stu-id="72d27-108">Example 1: Remove the AEM extension</span></span>
```
PS C:\> Remove-AzVMAEMExtension -ResourceGroupName "ResourceGroup11" -VMName "contoso-server"
```

<span data-ttu-id="72d27-109">To polecenie usuwa rozszerzenie AEM dla maszyny wirtualnej o nazwie contoso — serwer.</span><span class="sxs-lookup"><span data-stu-id="72d27-109">This command removes the AEM extension for the virtual machine named contoso-server.</span></span>

## <span data-ttu-id="72d27-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="72d27-110">PARAMETERS</span></span>

### <span data-ttu-id="72d27-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="72d27-111">-DefaultProfile</span></span>
<span data-ttu-id="72d27-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="72d27-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="72d27-113">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="72d27-113">-Name</span></span>
<span data-ttu-id="72d27-114">Określa nazwę maszyny wirtualnej, z której to polecenie cmdlet usuwa rozszerzenie AEM.</span><span class="sxs-lookup"><span data-stu-id="72d27-114">Specifies the name of the virtual machine from which this cmdlet removes the AEM extension.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ExtensionName

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="72d27-115">-Nowait</span><span class="sxs-lookup"><span data-stu-id="72d27-115">-NoWait</span></span>
<span data-ttu-id="72d27-116">Rozpoczyna operację i wraca natychmiast, zanim operacja zostanie ukończona.</span><span class="sxs-lookup"><span data-stu-id="72d27-116">Starts the operation and returns immediately, before the operation is completed.</span></span> <span data-ttu-id="72d27-117">W celu ustalenia, czy operacja została wykonana pomyślnie, użyj innego mechanizmu.</span><span class="sxs-lookup"><span data-stu-id="72d27-117">In order to determine if the operation has successfully been completed, use some other mechanism.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="72d27-118">-OSType</span><span class="sxs-lookup"><span data-stu-id="72d27-118">-OSType</span></span>
<span data-ttu-id="72d27-119">Określa typ systemu operacyjnego dysku systemu operacyjnego.</span><span class="sxs-lookup"><span data-stu-id="72d27-119">Specifies the type of the operating system of the operating system disk.</span></span>
<span data-ttu-id="72d27-120">Jeśli dysk systemu operacyjnego nie ma typu, należy określić ten parametr.</span><span class="sxs-lookup"><span data-stu-id="72d27-120">If the operating system disk does not have a type, you must specify this parameter.</span></span>
<span data-ttu-id="72d27-121">Dopuszczalne wartości tego parametru to: Windows i Linux.</span><span class="sxs-lookup"><span data-stu-id="72d27-121">The acceptable values for this parameter are: Windows and Linux.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="72d27-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="72d27-122">-ResourceGroupName</span></span>
<span data-ttu-id="72d27-123">Określa nazwę grupy zasobów maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="72d27-123">Specifies the name of the resource group of a virtual machine.</span></span>
<span data-ttu-id="72d27-124">To polecenie cmdlet usuwa rozszerzenie AEM z tej maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="72d27-124">This cmdlet removes the AEM extension from that virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="72d27-125">-VMName</span><span class="sxs-lookup"><span data-stu-id="72d27-125">-VMName</span></span>
<span data-ttu-id="72d27-126">Określa nazwę maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="72d27-126">Specifies the name of a virtual machine.</span></span>
<span data-ttu-id="72d27-127">To polecenie cmdlet usuwa rozszerzenie AEM dla maszyny wirtualnej, którą określa ten parametr.</span><span class="sxs-lookup"><span data-stu-id="72d27-127">This cmdlet removes the AEM extension for the virtual machine that this parameter specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="72d27-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="72d27-128">CommonParameters</span></span>
<span data-ttu-id="72d27-129">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="72d27-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="72d27-130">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="72d27-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="72d27-131">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="72d27-131">INPUTS</span></span>

### <span data-ttu-id="72d27-132">System. String</span><span class="sxs-lookup"><span data-stu-id="72d27-132">System.String</span></span>

## <span data-ttu-id="72d27-133">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="72d27-133">OUTPUTS</span></span>

### <span data-ttu-id="72d27-134">Microsoft. Azure. Commands. COMPUTE. models. PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="72d27-134">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="72d27-135">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="72d27-135">NOTES</span></span>

## <span data-ttu-id="72d27-136">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="72d27-136">RELATED LINKS</span></span>

[<span data-ttu-id="72d27-137">Get-AzVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="72d27-137">Get-AzVMAEMExtension</span></span>](./Get-AzVMAEMExtension.md)

[<span data-ttu-id="72d27-138">Set-AzVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="72d27-138">Set-AzVMAEMExtension</span></span>](./Set-AzVMAEMExtension.md)

[<span data-ttu-id="72d27-139">Test — AzVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="72d27-139">Test-AzVMAEMExtension</span></span>](./Test-AzVMAEMExtension.md)


