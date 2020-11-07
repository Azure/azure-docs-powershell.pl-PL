---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 32CF9DA7-5607-4CF9-A2D0-D76A0C005FDA
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/get-azurermvmaccessextension
schema: 2.0.0
ms.openlocfilehash: 5d07d90e7a9902713be3ef4d2acf3a2650e4f1b4
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/15/2020
ms.locfileid: "93898053"
---
# <span data-ttu-id="61bc8-101">Get-AzureRmVMAccessExtension</span><span class="sxs-lookup"><span data-stu-id="61bc8-101">Get-AzureRmVMAccessExtension</span></span>

## <span data-ttu-id="61bc8-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="61bc8-102">SYNOPSIS</span></span>
<span data-ttu-id="61bc8-103">Pobiera informacje o rozszerzeniu VMAccess.</span><span class="sxs-lookup"><span data-stu-id="61bc8-103">Gets information about the VMAccess extension.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="61bc8-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="61bc8-104">SYNTAX</span></span>

```
Get-AzureRmVMAccessExtension [-ResourceGroupName] <String> [-VMName] <String> [-Name] <String> [-Status]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="61bc8-105">Opis</span><span class="sxs-lookup"><span data-stu-id="61bc8-105">DESCRIPTION</span></span>
<span data-ttu-id="61bc8-106">Polecenie cmdlet **Get-AzureRmVMAccessExtension** pobiera informacje o rozszerzeniu maszyny wirtualnej dostępu do maszyny wirtualnej (VMAccess).</span><span class="sxs-lookup"><span data-stu-id="61bc8-106">The **Get-AzureRmVMAccessExtension** cmdlet gets information about the Virtual Machine Access (VMAccess) Virtual Machine Extension.</span></span>

## <span data-ttu-id="61bc8-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="61bc8-107">EXAMPLES</span></span>

### <span data-ttu-id="61bc8-108">Przykład 1: uzyskiwanie rozszerzenia VMAccess</span><span class="sxs-lookup"><span data-stu-id="61bc8-108">Example 1: Get the VMAccess extension</span></span>
```
PS C:\> $VMAccessExtension = Get-AzureRmVMAccessExtension -ResourceGroupName "ResourceGroup11" -VMName "VirtualMachine07" -Name "ContosoTest"
```

<span data-ttu-id="61bc8-109">To polecenie uzyskuje rozszerzenie VMAccess o nazwie ContosoTest dla maszyny wirtualnej o nazwie VirtualMachine07.</span><span class="sxs-lookup"><span data-stu-id="61bc8-109">This command gets the VMAccess extension named ContosoTest for the virtual machine named VirtualMachine07.</span></span>

### <span data-ttu-id="61bc8-110">Przykład 2: uzyskiwanie widoku wystąpienia rozszerzenia VMAccess</span><span class="sxs-lookup"><span data-stu-id="61bc8-110">Example 2: Get the instance view of the VMAccess extension</span></span>
```
PS C:\> $VMAccessExtension = Get-AzureRmVMAccessExtension -ResourceGroupName "ResourceGroup11" -VMName "VirtualMachine07" -Name "ContosoTest" -Status
```

<span data-ttu-id="61bc8-111">To polecenie pobiera widok wystąpienia rozszerzenia VMAccess o nazwie ContosoTest dla maszyny wirtualnej o nazwie VirtualMachine07.</span><span class="sxs-lookup"><span data-stu-id="61bc8-111">This command gets the instance view of the VMAccess extension named ContosoTest for the virtual machine named VirtualMachine07.</span></span>

## <span data-ttu-id="61bc8-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="61bc8-112">PARAMETERS</span></span>

### <span data-ttu-id="61bc8-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="61bc8-113">-DefaultProfile</span></span>
<span data-ttu-id="61bc8-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="61bc8-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="61bc8-115">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="61bc8-115">-Name</span></span>
<span data-ttu-id="61bc8-116">Określa nazwę rozszerzenia, które jest pobierane przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="61bc8-116">Specifies the name of the extension that this cmdlet gets.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ExtensionName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="61bc8-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="61bc8-117">-ResourceGroupName</span></span>
<span data-ttu-id="61bc8-118">Określa nazwę grupy zasobów maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="61bc8-118">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="61bc8-119">-Status</span><span class="sxs-lookup"><span data-stu-id="61bc8-119">-Status</span></span>
<span data-ttu-id="61bc8-120">Wskazuje, że ten aplet polecenia pobiera tylko widok wystąpienia rozszerzenia.</span><span class="sxs-lookup"><span data-stu-id="61bc8-120">Indicates that this cmdlet gets only the instance view of the extension.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="61bc8-121">-VMName</span><span class="sxs-lookup"><span data-stu-id="61bc8-121">-VMName</span></span>
<span data-ttu-id="61bc8-122">Określa nazwę maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="61bc8-122">Specifies the name of a virtual machine.</span></span>
<span data-ttu-id="61bc8-123">To polecenie cmdlet umożliwia pobieranie informacji o VMAccess dla maszyny wirtualnej określanej przez ten parametr.</span><span class="sxs-lookup"><span data-stu-id="61bc8-123">This cmdlet gets information about VMAccess for the virtual machine that this parameter specifies.</span></span>

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

### <span data-ttu-id="61bc8-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="61bc8-124">CommonParameters</span></span>
<span data-ttu-id="61bc8-125">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="61bc8-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="61bc8-126">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="61bc8-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="61bc8-127">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="61bc8-127">INPUTS</span></span>

### <span data-ttu-id="61bc8-128">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="61bc8-128">None</span></span>
<span data-ttu-id="61bc8-129">To polecenie cmdlet nie akceptuje żadnych danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="61bc8-129">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="61bc8-130">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="61bc8-130">OUTPUTS</span></span>

### <span data-ttu-id="61bc8-131">Microsoft. Azure. Commands. COMPUTE. models. VirtualMachineAccessExtensionContext</span><span class="sxs-lookup"><span data-stu-id="61bc8-131">Microsoft.Azure.Commands.Compute.Models.VirtualMachineAccessExtensionContext</span></span>

## <span data-ttu-id="61bc8-132">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="61bc8-132">NOTES</span></span>

## <span data-ttu-id="61bc8-133">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="61bc8-133">RELATED LINKS</span></span>

[<span data-ttu-id="61bc8-134">Remove-AzureRmVMAccessExtension</span><span class="sxs-lookup"><span data-stu-id="61bc8-134">Remove-AzureRmVMAccessExtension</span></span>](./Remove-AzureRmVMAccessExtension.md)

[<span data-ttu-id="61bc8-135">Set-AzureRmVMAccessExtension</span><span class="sxs-lookup"><span data-stu-id="61bc8-135">Set-AzureRmVMAccessExtension</span></span>](./Set-AzureRmVMAccessExtension.md)

[<span data-ttu-id="61bc8-136">Get-AzureRmVMExtension</span><span class="sxs-lookup"><span data-stu-id="61bc8-136">Get-AzureRmVMExtension</span></span>](./Get-AzureRmVMExtension.md)


