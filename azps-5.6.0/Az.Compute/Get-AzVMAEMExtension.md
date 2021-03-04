---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 212281F0-9A3E-4652-919F-400455E3950E
online version: https://docs.microsoft.com/powershell/module/az.compute/get-azvmaemextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMAEMExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMAEMExtension.md
ms.openlocfilehash: ed5f79763d8e9786f0a502f404474eeef2f641f6
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101958993"
---
# <span data-ttu-id="283ec-101">Get-AzVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="283ec-101">Get-AzVMAEMExtension</span></span>

## <span data-ttu-id="283ec-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="283ec-102">SYNOPSIS</span></span>
<span data-ttu-id="283ec-103">Pobiera informacje o rozszerzeniu AEM.</span><span class="sxs-lookup"><span data-stu-id="283ec-103">Gets information about the AEM extension.</span></span>

## <span data-ttu-id="283ec-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="283ec-104">SYNTAX</span></span>

```
Get-AzVMAEMExtension [-ResourceGroupName] <String> [-VMName] <String> [[-Name] <String>] [-Status]
 [[-OSType] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="283ec-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="283ec-105">DESCRIPTION</span></span>
<span data-ttu-id="283ec-106">Polecenie **cmdlet Get-AzVMAEMExtension** pobiera informacje o rozszerzeniu Azure Enhanced Monitoring (AEM).</span><span class="sxs-lookup"><span data-stu-id="283ec-106">The **Get-AzVMAEMExtension** cmdlet gets information about the Azure Enhanced Monitoring (AEM) extension.</span></span>

## <span data-ttu-id="283ec-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="283ec-107">EXAMPLES</span></span>

### <span data-ttu-id="283ec-108">Przykład 1. Uzyskiwanie rozszerzenia AEM</span><span class="sxs-lookup"><span data-stu-id="283ec-108">Example 1: Get the AEM extension</span></span>
```
PS C:\> Get-AzVMAEMExtension -ResourceGroupName "ResourceGroup11" -VMName "contoso-server"
```

<span data-ttu-id="283ec-109">To polecenie pobiera informacje dotyczące rozszerzenia AEM dla maszyny wirtualnej o nazwie contoso-server.</span><span class="sxs-lookup"><span data-stu-id="283ec-109">This command gets information for the AEM extension for the virtual machine named contoso-server.</span></span>

## <span data-ttu-id="283ec-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="283ec-110">PARAMETERS</span></span>

### <span data-ttu-id="283ec-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="283ec-111">-DefaultProfile</span></span>
<span data-ttu-id="283ec-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="283ec-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="283ec-113">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="283ec-113">-Name</span></span>
<span data-ttu-id="283ec-114">Określa nazwę maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="283ec-114">Specifies the name of a virtual machine.</span></span>
<span data-ttu-id="283ec-115">To polecenie cmdlet pobiera informacje dotyczące rozszerzenia AEM na maszyny wirtualnej, które określa to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="283ec-115">This cmdlet gets information for the AEM extension on the virtual machine that this cmdlet specifies.</span></span>

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

### <span data-ttu-id="283ec-116">- OSType</span><span class="sxs-lookup"><span data-stu-id="283ec-116">-OSType</span></span>
<span data-ttu-id="283ec-117">Określa typ systemu operacyjnego dysku systemu operacyjnego.</span><span class="sxs-lookup"><span data-stu-id="283ec-117">Specifies the type of the operating system of the operating system disk.</span></span>
<span data-ttu-id="283ec-118">Jeśli dysk systemu operacyjnego nie ma typu, musisz określić ten parametr.</span><span class="sxs-lookup"><span data-stu-id="283ec-118">If the operating system disk does not have a type, you must specify this parameter.</span></span>
<span data-ttu-id="283ec-119">Dopuszczalne wartości dla tego parametru to: Windows i Linux.</span><span class="sxs-lookup"><span data-stu-id="283ec-119">The acceptable values for this parameter are: Windows and Linux.</span></span>

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

### <span data-ttu-id="283ec-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="283ec-120">-ResourceGroupName</span></span>
<span data-ttu-id="283ec-121">Określa nazwę grupy zasobów maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="283ec-121">Specifies the name of the resource group of a virtual machine.</span></span>
<span data-ttu-id="283ec-122">To polecenie cmdlet pobiera informacje dotyczące rozszerzenia AEM na tej maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="283ec-122">This cmdlet gets information for the AEM extension on that virtual machine.</span></span>

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

### <span data-ttu-id="283ec-123">— Status</span><span class="sxs-lookup"><span data-stu-id="283ec-123">-Status</span></span>
<span data-ttu-id="283ec-124">Wskazuje, że to polecenie cmdlet pobiera tylko widok wystąpienia rozszerzenia AEM.</span><span class="sxs-lookup"><span data-stu-id="283ec-124">Indicates that this cmdlet gets only the instance view of the AEM extension.</span></span>

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

### <span data-ttu-id="283ec-125">-NAZWA.MASZYNY.WIRTUALNEJ</span><span class="sxs-lookup"><span data-stu-id="283ec-125">-VMName</span></span>
<span data-ttu-id="283ec-126">Określa nazwę maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="283ec-126">Specifies the name of a virtual machine.</span></span>
<span data-ttu-id="283ec-127">To polecenie cmdlet pobiera informacje o rozszerzeniu AEM dla maszyny wirtualnej, które określa ten parametr.</span><span class="sxs-lookup"><span data-stu-id="283ec-127">This cmdlet gets information about AEM extension for the virtual machine that this parameter specifies.</span></span>

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

### <span data-ttu-id="283ec-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="283ec-128">CommonParameters</span></span>
<span data-ttu-id="283ec-129">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="283ec-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="283ec-130">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="283ec-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="283ec-131">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="283ec-131">INPUTS</span></span>

### <span data-ttu-id="283ec-132">System.String</span><span class="sxs-lookup"><span data-stu-id="283ec-132">System.String</span></span>

### <span data-ttu-id="283ec-133">System.Management.Automation.SwitchParameters</span><span class="sxs-lookup"><span data-stu-id="283ec-133">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="283ec-134">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="283ec-134">OUTPUTS</span></span>

### <span data-ttu-id="283ec-135">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineExtension</span><span class="sxs-lookup"><span data-stu-id="283ec-135">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineExtension</span></span>

## <span data-ttu-id="283ec-136">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="283ec-136">NOTES</span></span>

## <span data-ttu-id="283ec-137">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="283ec-137">RELATED LINKS</span></span>

[<span data-ttu-id="283ec-138">Remove-AzVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="283ec-138">Remove-AzVMAEMExtension</span></span>](./Remove-AzVMAEMExtension.md)

[<span data-ttu-id="283ec-139">Set-AzVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="283ec-139">Set-AzVMAEMExtension</span></span>](./Set-AzVMAEMExtension.md)

[<span data-ttu-id="283ec-140">Test-AzVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="283ec-140">Test-AzVMAEMExtension</span></span>](./Test-AzVMAEMExtension.md)


