---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 9A6F140C-9F1C-4701-9603-FC6107FCAF92
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRmVMBootDiagnostics.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRmVMBootDiagnostics.md
ms.openlocfilehash: 32f5973668ca03dedb22b05186eda83002167648
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93525581"
---
# <span data-ttu-id="ccbf0-101">Set-AzureRmVMBootDiagnostics</span><span class="sxs-lookup"><span data-stu-id="ccbf0-101">Set-AzureRmVMBootDiagnostics</span></span>

## <span data-ttu-id="ccbf0-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="ccbf0-102">SYNOPSIS</span></span>
<span data-ttu-id="ccbf0-103">Modyfikowanie właściwości diagnostyki rozruchu maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="ccbf0-103">Modifies boot diagnostics properties of a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ccbf0-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="ccbf0-104">SYNTAX</span></span>

### <span data-ttu-id="ccbf0-105">EnableBootDiagnostics</span><span class="sxs-lookup"><span data-stu-id="ccbf0-105">EnableBootDiagnostics</span></span>
```
Set-AzureRmVMBootDiagnostics [-VM] <PSVirtualMachine> [-Enable] [-ResourceGroupName] <String>
 [[-StorageAccountName] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ccbf0-106">DisableBootDiagnostics</span><span class="sxs-lookup"><span data-stu-id="ccbf0-106">DisableBootDiagnostics</span></span>
```
Set-AzureRmVMBootDiagnostics [-VM] <PSVirtualMachine> [-Disable] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="ccbf0-107">Opis</span><span class="sxs-lookup"><span data-stu-id="ccbf0-107">DESCRIPTION</span></span>
<span data-ttu-id="ccbf0-108">Polecenie cmdlet **Set-AzureRmVMBootDiagnostics** modyfikuje właściwości diagnostyki rozruchu maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="ccbf0-108">The **Set-AzureRmVMBootDiagnostics** cmdlet modifies boot diagnostics properties of a virtual machine.</span></span>

## <span data-ttu-id="ccbf0-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="ccbf0-109">EXAMPLES</span></span>

### <span data-ttu-id="ccbf0-110">Przykład 1: Włączanie diagnostyki rozruchu</span><span class="sxs-lookup"><span data-stu-id="ccbf0-110">Example 1: Enable boot diagnostics</span></span>
```
PS C:\> $VM = Get-AzureRmVM -ResourceGroupName "ResourceGroup11" -Name "ContosoVM07"
PS C:\> Set-AzureRmVMBootDiagnostics -VM $VM -Enable -ResourceGroupName "ResourceGroup11" -StorageAccountName "DiagnosticStorage"
```

<span data-ttu-id="ccbf0-111">Pierwsze polecenie uzyskuje maszynę wirtualną o nazwie ContosoVM07 przy użyciu polecenia **Get-AzureRmVM**.</span><span class="sxs-lookup"><span data-stu-id="ccbf0-111">The first command gets the virtual machine named ContosoVM07 by using **Get-AzureRmVM**.</span></span>
<span data-ttu-id="ccbf0-112">Polecenie zapisuje je w zmiennej $VM.</span><span class="sxs-lookup"><span data-stu-id="ccbf0-112">The command stores it in the $VM variable.</span></span>

<span data-ttu-id="ccbf0-113">Drugie polecenie włącza diagnostykę rozruchu maszyny wirtualnej w $VM.</span><span class="sxs-lookup"><span data-stu-id="ccbf0-113">The second command enables boot diagnostics for the virtual machine in $VM.</span></span>
<span data-ttu-id="ccbf0-114">Dane diagnostyczne są przechowywane na określonym koncie.</span><span class="sxs-lookup"><span data-stu-id="ccbf0-114">Diagnostics data is stored in the specified account.</span></span>

## <span data-ttu-id="ccbf0-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="ccbf0-115">PARAMETERS</span></span>

### <span data-ttu-id="ccbf0-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ccbf0-116">-DefaultProfile</span></span>
<span data-ttu-id="ccbf0-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="ccbf0-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ccbf0-118">-Disable</span><span class="sxs-lookup"><span data-stu-id="ccbf0-118">-Disable</span></span>
<span data-ttu-id="ccbf0-119">Wskazuje, że to polecenie cmdlet wyłącza diagnostykę rozruchu maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="ccbf0-119">Indicates that this cmdlet disables the boot diagnostics for the virtual machine.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: DisableBootDiagnostics
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ccbf0-120">-Enable</span><span class="sxs-lookup"><span data-stu-id="ccbf0-120">-Enable</span></span>
<span data-ttu-id="ccbf0-121">Wskazuje, że to polecenie cmdlet włącza diagnostykę rozruchu maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="ccbf0-121">Indicates that this cmdlet enables the boot diagnostics for the virtual machine.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: EnableBootDiagnostics
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ccbf0-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ccbf0-122">-ResourceGroupName</span></span>
<span data-ttu-id="ccbf0-123">Określa nazwę grupy zasobów maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="ccbf0-123">Specifies the name of the resource group of the virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: EnableBootDiagnostics
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ccbf0-124">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="ccbf0-124">-StorageAccountName</span></span>
<span data-ttu-id="ccbf0-125">Określa nazwę konta magazynu, w którym mają być zapisywane dane diagnostyczne rozruchu.</span><span class="sxs-lookup"><span data-stu-id="ccbf0-125">Specifies the name of the storage account in which to save boot diagnostics data.</span></span>

```yaml
Type: System.String
Parameter Sets: EnableBootDiagnostics
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ccbf0-126">-VM</span><span class="sxs-lookup"><span data-stu-id="ccbf0-126">-VM</span></span>
<span data-ttu-id="ccbf0-127">Określa maszynę wirtualną, dla której to polecenie cmdlet zmienia narzędzie diagnostyczne rozruchu.</span><span class="sxs-lookup"><span data-stu-id="ccbf0-127">Specifies the virtual machine for which this cmdlet changes boot diagnostics.</span></span>
<span data-ttu-id="ccbf0-128">Aby uzyskać obiekt maszyny wirtualnej, użyj polecenia cmdlet Get-AzureRmVM.</span><span class="sxs-lookup"><span data-stu-id="ccbf0-128">To obtain a virtual machine object, use the Get-AzureRmVM cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine
Parameter Sets: (All)
Aliases: VMProfile

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ccbf0-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ccbf0-129">CommonParameters</span></span>
<span data-ttu-id="ccbf0-130">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ccbf0-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ccbf0-131">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ccbf0-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ccbf0-132">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ccbf0-132">INPUTS</span></span>

## <span data-ttu-id="ccbf0-133">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="ccbf0-133">OUTPUTS</span></span>

## <span data-ttu-id="ccbf0-134">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="ccbf0-134">NOTES</span></span>

## <span data-ttu-id="ccbf0-135">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="ccbf0-135">RELATED LINKS</span></span>

[<span data-ttu-id="ccbf0-136">Get-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="ccbf0-136">Get-AzureRmVM</span></span>](./Get-AzureRmVM.md)

[<span data-ttu-id="ccbf0-137">Get-AzureRmVMBootDiagnosticsData</span><span class="sxs-lookup"><span data-stu-id="ccbf0-137">Get-AzureRmVMBootDiagnosticsData</span></span>](./Get-AzureRmVMBootDiagnosticsData.md)

