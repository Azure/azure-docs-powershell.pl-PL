---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: F41953F1-9515-4081-8624-6A1494DA4BB2
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azvmchefextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMChefExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMChefExtension.md
ms.openlocfilehash: 02647fc2148069e2c408c979e4b258fd0a641fc0
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/27/2020
ms.locfileid: "94224588"
---
# <span data-ttu-id="d8202-101">Get-AzVMChefExtension</span><span class="sxs-lookup"><span data-stu-id="d8202-101">Get-AzVMChefExtension</span></span>

## <span data-ttu-id="d8202-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="d8202-102">SYNOPSIS</span></span>
<span data-ttu-id="d8202-103">Pobiera informacje o rozszerzeniu Kuchmistrz.</span><span class="sxs-lookup"><span data-stu-id="d8202-103">Gets information about a Chef extension.</span></span>

## <span data-ttu-id="d8202-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="d8202-104">SYNTAX</span></span>

### <span data-ttu-id="d8202-105">Linux</span><span class="sxs-lookup"><span data-stu-id="d8202-105">Linux</span></span>
```
Get-AzVMChefExtension [-ResourceGroupName] <String> [-VMName] <String> [[-Name] <String>] [-Status] [-Linux]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d8202-106">Microsoft</span><span class="sxs-lookup"><span data-stu-id="d8202-106">Windows</span></span>
```
Get-AzVMChefExtension [-ResourceGroupName] <String> [-VMName] <String> [[-Name] <String>] [-Status] [-Windows]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d8202-107">Opis</span><span class="sxs-lookup"><span data-stu-id="d8202-107">DESCRIPTION</span></span>
<span data-ttu-id="d8202-108">Polecenie cmdlet **Get-AzVMChefExtension** pobiera informacje o rozszerzeniu Kuchmistrz zainstalowanym na maszynie wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="d8202-108">The **Get-AzVMChefExtension** cmdlet gets information about a Chef extension installed on a virtual machine.</span></span>

## <span data-ttu-id="d8202-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="d8202-109">EXAMPLES</span></span>

### <span data-ttu-id="d8202-110">Przykład 1: uzyskiwanie szczegółowych informacji o rozszerzeniu Kuchmistrz dla maszyny wirtualnej systemu Windows</span><span class="sxs-lookup"><span data-stu-id="d8202-110">Example 1: Get the details of Chef extension for a Windows virtual machine</span></span>
```
PS C:\> Get-AzVMChefExtension -ResourceGroupName "ResourceGroup001" -VMName "WindowsVM001" -Windows
```

<span data-ttu-id="d8202-111">To polecenie pobiera rozszerzenie Kuchmistrz z maszyny wirtualnej systemu Windows o nazwie WindowsVM001 należącej do grupy zasobów o nazwie ResourceGroup001.</span><span class="sxs-lookup"><span data-stu-id="d8202-111">This command gets the Chef extension from a Windows virtual machine named WindowsVM001 that belongs to the resource group named ResourceGroup001.</span></span>

### <span data-ttu-id="d8202-112">Przykład 2: uzyskiwanie szczegółowych informacji o rozszerzeniu Kuchmistrz dla maszyny wirtualnej Linux</span><span class="sxs-lookup"><span data-stu-id="d8202-112">Example 2: Get the details of Chef extension for a Linux virtual machine</span></span>
```
PS C:\> Get-AzVMChefExtension -ResourceGroupName "ResourceGroup002" -VMName "LinuxVM001" -Linux
```

<span data-ttu-id="d8202-113">To polecenie pobiera rozszerzenie Kuchmistrz z maszyny wirtualnej Linux o nazwie LinuxVM001 należącej do grupy zasobów o nazwie ResourceGroup002.</span><span class="sxs-lookup"><span data-stu-id="d8202-113">This command gets the Chef extension from a Linux virtual machine named LinuxVM001 that belongs to the resource group named ResourceGroup002.</span></span>

## <span data-ttu-id="d8202-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="d8202-114">PARAMETERS</span></span>

### <span data-ttu-id="d8202-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d8202-115">-DefaultProfile</span></span>
<span data-ttu-id="d8202-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="d8202-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d8202-117">-Linux</span><span class="sxs-lookup"><span data-stu-id="d8202-117">-Linux</span></span>
<span data-ttu-id="d8202-118">Wskazuje, że to polecenie cmdlet działa na maszynie wirtualnej Linux.</span><span class="sxs-lookup"><span data-stu-id="d8202-118">Indicates that this cmdlet works on a Linux virtual machine.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Linux
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d8202-119">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="d8202-119">-Name</span></span>
<span data-ttu-id="d8202-120">Określa nazwę rozszerzenia Kuchmistrz.</span><span class="sxs-lookup"><span data-stu-id="d8202-120">Specifies the name of the Chef extension.</span></span>

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

### <span data-ttu-id="d8202-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d8202-121">-ResourceGroupName</span></span>
<span data-ttu-id="d8202-122">Określa nazwę grupy zasobów zawierającej maszynę wirtualną.</span><span class="sxs-lookup"><span data-stu-id="d8202-122">Specifies the name of the resource group that contains the virtual machine.</span></span>

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

### <span data-ttu-id="d8202-123">-Status</span><span class="sxs-lookup"><span data-stu-id="d8202-123">-Status</span></span>
<span data-ttu-id="d8202-124">Wskazuje, że to polecenie cmdlet pobiera tylko widok wystąpienia rozszerzenia Kuchmistrz.</span><span class="sxs-lookup"><span data-stu-id="d8202-124">Indicates that this cmdlet gets only the instance view of the Chef extension.</span></span>

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

### <span data-ttu-id="d8202-125">-VMName</span><span class="sxs-lookup"><span data-stu-id="d8202-125">-VMName</span></span>
<span data-ttu-id="d8202-126">Określa nazwę maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="d8202-126">Specifies the name of a virtual machine.</span></span>

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

### <span data-ttu-id="d8202-127">-Windows</span><span class="sxs-lookup"><span data-stu-id="d8202-127">-Windows</span></span>
<span data-ttu-id="d8202-128">Wskazuje, że to polecenie cmdlet dotyczy maszyny wirtualnej systemu Windows.</span><span class="sxs-lookup"><span data-stu-id="d8202-128">Indicates that this cmdlet is for a Windows virtual machine.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Windows
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d8202-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d8202-129">CommonParameters</span></span>
<span data-ttu-id="d8202-130">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d8202-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d8202-131">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d8202-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d8202-132">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d8202-132">INPUTS</span></span>

### <span data-ttu-id="d8202-133">System. String</span><span class="sxs-lookup"><span data-stu-id="d8202-133">System.String</span></span>

### <span data-ttu-id="d8202-134">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="d8202-134">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="d8202-135">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="d8202-135">OUTPUTS</span></span>

### <span data-ttu-id="d8202-136">Microsoft. Azure. Commands. COMPUTE. models. PSVirtualMachineExtension</span><span class="sxs-lookup"><span data-stu-id="d8202-136">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineExtension</span></span>

## <span data-ttu-id="d8202-137">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="d8202-137">NOTES</span></span>

## <span data-ttu-id="d8202-138">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="d8202-138">RELATED LINKS</span></span>

[<span data-ttu-id="d8202-139">Set-AzVMChefExtension</span><span class="sxs-lookup"><span data-stu-id="d8202-139">Set-AzVMChefExtension</span></span>](./Set-AzVMChefExtension.md)

[<span data-ttu-id="d8202-140">Remove-AzVMChefExtension</span><span class="sxs-lookup"><span data-stu-id="d8202-140">Remove-AzVMChefExtension</span></span>](./Remove-AzVMChefExtension.md)


