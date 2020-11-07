---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 9A6F140C-9F1C-4701-9603-FC6107FCAF92
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/set-azurermvmbootdiagnostics
schema: 2.0.0
ms.openlocfilehash: 2faa28fc0f0e4c27e384c178b96b8d38cae16a3d
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/15/2020
ms.locfileid: "93898938"
---
# <span data-ttu-id="d1fd7-101">Set-AzureRmVMBootDiagnostics</span><span class="sxs-lookup"><span data-stu-id="d1fd7-101">Set-AzureRmVMBootDiagnostics</span></span>

## <span data-ttu-id="d1fd7-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="d1fd7-102">SYNOPSIS</span></span>
<span data-ttu-id="d1fd7-103">Modyfikowanie właściwości diagnostyki rozruchu maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="d1fd7-103">Modifies boot diagnostics properties of a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d1fd7-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="d1fd7-104">SYNTAX</span></span>

### <span data-ttu-id="d1fd7-105">EnableBootDiagnostics</span><span class="sxs-lookup"><span data-stu-id="d1fd7-105">EnableBootDiagnostics</span></span>
```
Set-AzureRmVMBootDiagnostics [-VM] <PSVirtualMachine> [-Enable] [-ResourceGroupName] <String>
 [[-StorageAccountName] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d1fd7-106">DisableBootDiagnostics</span><span class="sxs-lookup"><span data-stu-id="d1fd7-106">DisableBootDiagnostics</span></span>
```
Set-AzureRmVMBootDiagnostics [-VM] <PSVirtualMachine> [-Disable] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="d1fd7-107">Opis</span><span class="sxs-lookup"><span data-stu-id="d1fd7-107">DESCRIPTION</span></span>
<span data-ttu-id="d1fd7-108">Polecenie cmdlet **Set-AzureRmVMBootDiagnostics** modyfikuje właściwości diagnostyki rozruchu maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="d1fd7-108">The **Set-AzureRmVMBootDiagnostics** cmdlet modifies boot diagnostics properties of a virtual machine.</span></span>

## <span data-ttu-id="d1fd7-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="d1fd7-109">EXAMPLES</span></span>

### <span data-ttu-id="d1fd7-110">Przykład 1: Włączanie diagnostyki rozruchu</span><span class="sxs-lookup"><span data-stu-id="d1fd7-110">Example 1: Enable boot diagnostics</span></span>
```
PS C:\> $VM = Get-AzureRmVM -ResourceGroupName "ResourceGroup11" -Name "ContosoVM07"
PS C:\> Set-AzureRmVMBootDiagnostics -VM $VM -Enable -ResourceGroupName "ResourceGroup11" -StorageAccountName "DiagnosticStorage"
```

<span data-ttu-id="d1fd7-111">Pierwsze polecenie uzyskuje maszynę wirtualną o nazwie ContosoVM07 przy użyciu polecenia **Get-AzureRmVM**.</span><span class="sxs-lookup"><span data-stu-id="d1fd7-111">The first command gets the virtual machine named ContosoVM07 by using **Get-AzureRmVM**.</span></span>
<span data-ttu-id="d1fd7-112">Polecenie zapisuje je w zmiennej $VM.</span><span class="sxs-lookup"><span data-stu-id="d1fd7-112">The command stores it in the $VM variable.</span></span>

<span data-ttu-id="d1fd7-113">Drugie polecenie włącza diagnostykę rozruchu maszyny wirtualnej w $VM.</span><span class="sxs-lookup"><span data-stu-id="d1fd7-113">The second command enables boot diagnostics for the virtual machine in $VM.</span></span>
<span data-ttu-id="d1fd7-114">Dane diagnostyczne są przechowywane na określonym koncie.</span><span class="sxs-lookup"><span data-stu-id="d1fd7-114">Diagnostics data is stored in the specified account.</span></span>

## <span data-ttu-id="d1fd7-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="d1fd7-115">PARAMETERS</span></span>

### <span data-ttu-id="d1fd7-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d1fd7-116">-DefaultProfile</span></span>
<span data-ttu-id="d1fd7-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="d1fd7-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d1fd7-118">-Disable</span><span class="sxs-lookup"><span data-stu-id="d1fd7-118">-Disable</span></span>
<span data-ttu-id="d1fd7-119">Wskazuje, że to polecenie cmdlet wyłącza diagnostykę rozruchu maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="d1fd7-119">Indicates that this cmdlet disables the boot diagnostics for the virtual machine.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: DisableBootDiagnostics
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d1fd7-120">-Enable</span><span class="sxs-lookup"><span data-stu-id="d1fd7-120">-Enable</span></span>
<span data-ttu-id="d1fd7-121">Wskazuje, że to polecenie cmdlet włącza diagnostykę rozruchu maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="d1fd7-121">Indicates that this cmdlet enables the boot diagnostics for the virtual machine.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: EnableBootDiagnostics
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d1fd7-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d1fd7-122">-ResourceGroupName</span></span>
<span data-ttu-id="d1fd7-123">Określa nazwę grupy zasobów maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="d1fd7-123">Specifies the name of the resource group of the virtual machine.</span></span>

```yaml
Type: String
Parameter Sets: EnableBootDiagnostics
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d1fd7-124">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="d1fd7-124">-StorageAccountName</span></span>
<span data-ttu-id="d1fd7-125">Określa nazwę konta magazynu, w którym mają być zapisywane dane diagnostyczne rozruchu.</span><span class="sxs-lookup"><span data-stu-id="d1fd7-125">Specifies the name of the storage account in which to save boot diagnostics data.</span></span>

```yaml
Type: String
Parameter Sets: EnableBootDiagnostics
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d1fd7-126">-VM</span><span class="sxs-lookup"><span data-stu-id="d1fd7-126">-VM</span></span>
<span data-ttu-id="d1fd7-127">Określa maszynę wirtualną, dla której to polecenie cmdlet zmienia narzędzie diagnostyczne rozruchu.</span><span class="sxs-lookup"><span data-stu-id="d1fd7-127">Specifies the virtual machine for which this cmdlet changes boot diagnostics.</span></span>
<span data-ttu-id="d1fd7-128">Aby uzyskać obiekt maszyny wirtualnej, użyj polecenia cmdlet Get-AzureRmVM.</span><span class="sxs-lookup"><span data-stu-id="d1fd7-128">To obtain a virtual machine object, use the Get-AzureRmVM cmdlet.</span></span>

```yaml
Type: PSVirtualMachine
Parameter Sets: (All)
Aliases: VMProfile

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d1fd7-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d1fd7-129">CommonParameters</span></span>
<span data-ttu-id="d1fd7-130">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d1fd7-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d1fd7-131">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d1fd7-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d1fd7-132">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d1fd7-132">INPUTS</span></span>

### <span data-ttu-id="d1fd7-133">PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="d1fd7-133">PSVirtualMachine</span></span>
<span data-ttu-id="d1fd7-134">Parametr "VM" akceptuje wartość typu "PSVirtualMachine" z procesu</span><span class="sxs-lookup"><span data-stu-id="d1fd7-134">Parameter 'VM' accepts value of type 'PSVirtualMachine' from the pipeline</span></span>

## <span data-ttu-id="d1fd7-135">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="d1fd7-135">OUTPUTS</span></span>

### <span data-ttu-id="d1fd7-136">Microsoft. Azure. Commands. COMPUTE. models. PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="d1fd7-136">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

## <span data-ttu-id="d1fd7-137">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="d1fd7-137">NOTES</span></span>

## <span data-ttu-id="d1fd7-138">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="d1fd7-138">RELATED LINKS</span></span>

[<span data-ttu-id="d1fd7-139">Get-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="d1fd7-139">Get-AzureRmVM</span></span>](./Get-AzureRmVM.md)

[<span data-ttu-id="d1fd7-140">Get-AzureRmVMBootDiagnosticsData</span><span class="sxs-lookup"><span data-stu-id="d1fd7-140">Get-AzureRmVMBootDiagnosticsData</span></span>](./Get-AzureRmVMBootDiagnosticsData.md)


