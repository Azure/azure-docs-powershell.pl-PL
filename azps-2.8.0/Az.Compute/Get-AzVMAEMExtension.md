---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 212281F0-9A3E-4652-919F-400455E3950E
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azvmaemextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMAEMExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMAEMExtension.md
ms.openlocfilehash: 8cd67aa715b0092c82a3553158a4736d8f1e850e
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93706421"
---
# <span data-ttu-id="46a80-101">Get-AzVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="46a80-101">Get-AzVMAEMExtension</span></span>

## <span data-ttu-id="46a80-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="46a80-102">SYNOPSIS</span></span>
<span data-ttu-id="46a80-103">Pobiera informacje o rozszerzeniu AEM.</span><span class="sxs-lookup"><span data-stu-id="46a80-103">Gets information about the AEM extension.</span></span>

## <span data-ttu-id="46a80-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="46a80-104">SYNTAX</span></span>

```
Get-AzVMAEMExtension [-ResourceGroupName] <String> [-VMName] <String> [[-Name] <String>] [-Status]
 [[-OSType] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="46a80-105">Opis</span><span class="sxs-lookup"><span data-stu-id="46a80-105">DESCRIPTION</span></span>
<span data-ttu-id="46a80-106">Polecenie cmdlet **Get-AzVMAEMExtension** pobiera informacje o rozszerzeniu usługi Azure enhanceing Monitoring (AEM).</span><span class="sxs-lookup"><span data-stu-id="46a80-106">The **Get-AzVMAEMExtension** cmdlet gets information about the Azure Enhanced Monitoring (AEM) extension.</span></span>

## <span data-ttu-id="46a80-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="46a80-107">EXAMPLES</span></span>

### <span data-ttu-id="46a80-108">Przykład 1: uzyskiwanie rozszerzenia AEM</span><span class="sxs-lookup"><span data-stu-id="46a80-108">Example 1: Get the AEM extension</span></span>
```
PS C:\> Get-AzVMAEMExtension -ResourceGroupName "ResourceGroup11" -VMName "contoso-server"
```

<span data-ttu-id="46a80-109">To polecenie pobiera informacje o rozszerzeniu AEM dla maszyny wirtualnej o nazwie contoso — Server.</span><span class="sxs-lookup"><span data-stu-id="46a80-109">This command gets information for the AEM extension for the virtual machine named contoso-server.</span></span>

## <span data-ttu-id="46a80-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="46a80-110">PARAMETERS</span></span>

### <span data-ttu-id="46a80-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="46a80-111">-DefaultProfile</span></span>
<span data-ttu-id="46a80-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="46a80-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="46a80-113">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="46a80-113">-Name</span></span>
<span data-ttu-id="46a80-114">Określa nazwę maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="46a80-114">Specifies the name of a virtual machine.</span></span>
<span data-ttu-id="46a80-115">To polecenie cmdlet umożliwia pobieranie informacji dotyczących rozszerzenia AEM na maszynie wirtualnej, którą to polecenie cmdlet określa.</span><span class="sxs-lookup"><span data-stu-id="46a80-115">This cmdlet gets information for the AEM extension on the virtual machine that this cmdlet specifies.</span></span>

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

### <span data-ttu-id="46a80-116">-OSType</span><span class="sxs-lookup"><span data-stu-id="46a80-116">-OSType</span></span>
<span data-ttu-id="46a80-117">Określa typ systemu operacyjnego dysku systemu operacyjnego.</span><span class="sxs-lookup"><span data-stu-id="46a80-117">Specifies the type of the operating system of the operating system disk.</span></span>
<span data-ttu-id="46a80-118">Jeśli dysk systemu operacyjnego nie ma typu, należy określić ten parametr.</span><span class="sxs-lookup"><span data-stu-id="46a80-118">If the operating system disk does not have a type, you must specify this parameter.</span></span>
<span data-ttu-id="46a80-119">Dopuszczalne wartości tego parametru to: Windows i Linux.</span><span class="sxs-lookup"><span data-stu-id="46a80-119">The acceptable values for this parameter are: Windows and Linux.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="46a80-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="46a80-120">-ResourceGroupName</span></span>
<span data-ttu-id="46a80-121">Określa nazwę grupy zasobów maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="46a80-121">Specifies the name of the resource group of a virtual machine.</span></span>
<span data-ttu-id="46a80-122">To polecenie cmdlet umożliwia pobieranie informacji dotyczących rozszerzenia AEM na tej maszynie wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="46a80-122">This cmdlet gets information for the AEM extension on that virtual machine.</span></span>

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

### <span data-ttu-id="46a80-123">-Status</span><span class="sxs-lookup"><span data-stu-id="46a80-123">-Status</span></span>
<span data-ttu-id="46a80-124">Wskazuje, że to polecenie cmdlet pobiera tylko widok wystąpienia rozszerzenia AEM.</span><span class="sxs-lookup"><span data-stu-id="46a80-124">Indicates that this cmdlet gets only the instance view of the AEM extension.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="46a80-125">-VMName</span><span class="sxs-lookup"><span data-stu-id="46a80-125">-VMName</span></span>
<span data-ttu-id="46a80-126">Określa nazwę maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="46a80-126">Specifies the name of a virtual machine.</span></span>
<span data-ttu-id="46a80-127">To polecenie cmdlet umożliwia pobieranie informacji o rozszerzeniu AEM dla maszyny wirtualnej, którą ten parametr określa.</span><span class="sxs-lookup"><span data-stu-id="46a80-127">This cmdlet gets information about AEM extension for the virtual machine that this parameter specifies.</span></span>

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

### <span data-ttu-id="46a80-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="46a80-128">CommonParameters</span></span>
<span data-ttu-id="46a80-129">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="46a80-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="46a80-130">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="46a80-130">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="46a80-131">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="46a80-131">INPUTS</span></span>

### <span data-ttu-id="46a80-132">System. String</span><span class="sxs-lookup"><span data-stu-id="46a80-132">System.String</span></span>

### <span data-ttu-id="46a80-133">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="46a80-133">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="46a80-134">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="46a80-134">OUTPUTS</span></span>

### <span data-ttu-id="46a80-135">Microsoft. Azure. Commands. COMPUTE. models. PSVirtualMachineExtension</span><span class="sxs-lookup"><span data-stu-id="46a80-135">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineExtension</span></span>

## <span data-ttu-id="46a80-136">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="46a80-136">NOTES</span></span>

## <span data-ttu-id="46a80-137">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="46a80-137">RELATED LINKS</span></span>

[<span data-ttu-id="46a80-138">Remove-AzVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="46a80-138">Remove-AzVMAEMExtension</span></span>](./Remove-AzVMAEMExtension.md)

[<span data-ttu-id="46a80-139">Set-AzVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="46a80-139">Set-AzVMAEMExtension</span></span>](./Set-AzVMAEMExtension.md)

[<span data-ttu-id="46a80-140">Test — AzVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="46a80-140">Test-AzVMAEMExtension</span></span>](./Test-AzVMAEMExtension.md)


