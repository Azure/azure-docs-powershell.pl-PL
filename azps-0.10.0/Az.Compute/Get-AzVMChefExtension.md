---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
ms.assetid: F41953F1-9515-4081-8624-6A1494DA4BB2
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azvmchefextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Get-AzVMChefExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Get-AzVMChefExtension.md
ms.openlocfilehash: fe6f65aa2e673007b3eda52134c42782c7a49bd9
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/16/2020
ms.locfileid: "93893782"
---
# <span data-ttu-id="40cec-101">Get-AzVMChefExtension</span><span class="sxs-lookup"><span data-stu-id="40cec-101">Get-AzVMChefExtension</span></span>

## <span data-ttu-id="40cec-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="40cec-102">SYNOPSIS</span></span>
<span data-ttu-id="40cec-103">Pobiera informacje o rozszerzeniu Kuchmistrz.</span><span class="sxs-lookup"><span data-stu-id="40cec-103">Gets information about a Chef extension.</span></span>

## <span data-ttu-id="40cec-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="40cec-104">SYNTAX</span></span>

### <span data-ttu-id="40cec-105">Linux</span><span class="sxs-lookup"><span data-stu-id="40cec-105">Linux</span></span>
```
Get-AzVMChefExtension [-ResourceGroupName] <String> [-VMName] <String> [[-Name] <String>] [-Status]
 [-Linux] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="40cec-106">Microsoft</span><span class="sxs-lookup"><span data-stu-id="40cec-106">Windows</span></span>
```
Get-AzVMChefExtension [-ResourceGroupName] <String> [-VMName] <String> [[-Name] <String>] [-Status]
 [-Windows] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="40cec-107">Opis</span><span class="sxs-lookup"><span data-stu-id="40cec-107">DESCRIPTION</span></span>
<span data-ttu-id="40cec-108">Polecenie cmdlet **Get-AzureVMChefExtension** pobiera informacje o rozszerzeniu Kuchmistrz zainstalowanym na maszynie wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="40cec-108">The **Get-AzureVMChefExtension** cmdlet gets information about a Chef extension installed on a virtual machine.</span></span>

## <span data-ttu-id="40cec-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="40cec-109">EXAMPLES</span></span>

### <span data-ttu-id="40cec-110">Przykład 1: uzyskiwanie szczegółowych informacji o rozszerzeniu Kuchmistrz dla maszyny wirtualnej systemu Windows</span><span class="sxs-lookup"><span data-stu-id="40cec-110">Example 1: Get the details of Chef extension for a Windows virtual machine-</span></span>
```
PS C:\> Get-AzVMChefExtension -ResourceGroupName "ResourceGroup001" -VMName "WindowsVM001" -Windows
```

<span data-ttu-id="40cec-111">To polecenie pobiera rozszerzenie Kuchmistrz z maszyny wirtualnej systemu Windows o nazwie WindowsVM001 należącej do grupy zasobów o nazwie ResourceGroup001.</span><span class="sxs-lookup"><span data-stu-id="40cec-111">This command gets the Chef extension from a Windows virtual machine named WindowsVM001 that belongs to the resource group named ResourceGroup001.</span></span>

### <span data-ttu-id="40cec-112">Przykład 2: uzyskiwanie szczegółowych informacji o rozszerzeniu Kuchmistrz dla maszyny wirtualnej Linux</span><span class="sxs-lookup"><span data-stu-id="40cec-112">Example 2: Get the details of Chef extension for a Linux virtual machine</span></span>
```
PS C:\> Get-AzVMChefExtension -ResourceGroupName "ResourceGroup002" -VMName "LinuxVM001" -Linux
```

<span data-ttu-id="40cec-113">To polecenie pobiera rozszerzenie Kuchmistrz z maszyny wirtualnej Linux o nazwie LinuxVM001 należącej do grupy zasobów o nazwie ResourceGroup002.</span><span class="sxs-lookup"><span data-stu-id="40cec-113">This command gets the Chef extension from a Linux virtual machine named LinuxVM001 that belongs to the resource group named ResourceGroup002.</span></span>

## <span data-ttu-id="40cec-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="40cec-114">PARAMETERS</span></span>

### <span data-ttu-id="40cec-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="40cec-115">-DefaultProfile</span></span>
<span data-ttu-id="40cec-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="40cec-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="40cec-117">-Linux</span><span class="sxs-lookup"><span data-stu-id="40cec-117">-Linux</span></span>
<span data-ttu-id="40cec-118">Wskazuje, że to polecenie cmdlet działa na maszynie wirtualnej Linux.</span><span class="sxs-lookup"><span data-stu-id="40cec-118">Indicates that this cmdlet works on a Linux virtual machine.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: Linux
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="40cec-119">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="40cec-119">-Name</span></span>
<span data-ttu-id="40cec-120">Określa nazwę rozszerzenia Kuchmistrz.</span><span class="sxs-lookup"><span data-stu-id="40cec-120">Specifies the name of the Chef extension.</span></span>

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

### <span data-ttu-id="40cec-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="40cec-121">-ResourceGroupName</span></span>
<span data-ttu-id="40cec-122">Określa nazwę grupy zasobów zawierającej maszynę wirtualną.</span><span class="sxs-lookup"><span data-stu-id="40cec-122">Specifies the name of the resource group that contains the virtual machine.</span></span>

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

### <span data-ttu-id="40cec-123">-Status</span><span class="sxs-lookup"><span data-stu-id="40cec-123">-Status</span></span>
<span data-ttu-id="40cec-124">Wskazuje, że to polecenie cmdlet pobiera tylko widok wystąpienia rozszerzenia Kuchmistrz.</span><span class="sxs-lookup"><span data-stu-id="40cec-124">Indicates that this cmdlet gets only the instance view of the Chef extension.</span></span>

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

### <span data-ttu-id="40cec-125">-VMName</span><span class="sxs-lookup"><span data-stu-id="40cec-125">-VMName</span></span>
<span data-ttu-id="40cec-126">Określa nazwę maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="40cec-126">Specifies the name of a virtual machine.</span></span>

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

### <span data-ttu-id="40cec-127">-Windows</span><span class="sxs-lookup"><span data-stu-id="40cec-127">-Windows</span></span>
<span data-ttu-id="40cec-128">Wskazuje, że to polecenie cmdlet dotyczy maszyny wirtualnej systemu Windows.</span><span class="sxs-lookup"><span data-stu-id="40cec-128">Indicates that this cmdlet is for a Windows virtual machine.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: Windows
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="40cec-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="40cec-129">CommonParameters</span></span>
<span data-ttu-id="40cec-130">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="40cec-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="40cec-131">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="40cec-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="40cec-132">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="40cec-132">INPUTS</span></span>

### <span data-ttu-id="40cec-133">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="40cec-133">None</span></span>
<span data-ttu-id="40cec-134">To polecenie cmdlet nie akceptuje żadnych danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="40cec-134">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="40cec-135">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="40cec-135">OUTPUTS</span></span>

### <span data-ttu-id="40cec-136">Microsoft. Azure. Commands. COMPUTE. models. PSVirtualMachineExtension</span><span class="sxs-lookup"><span data-stu-id="40cec-136">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineExtension</span></span>

## <span data-ttu-id="40cec-137">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="40cec-137">NOTES</span></span>

## <span data-ttu-id="40cec-138">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="40cec-138">RELATED LINKS</span></span>

[<span data-ttu-id="40cec-139">Set-AzVMChefExtension</span><span class="sxs-lookup"><span data-stu-id="40cec-139">Set-AzVMChefExtension</span></span>](./Set-AzVMChefExtension.md)

[<span data-ttu-id="40cec-140">Remove-AzVMChefExtension</span><span class="sxs-lookup"><span data-stu-id="40cec-140">Remove-AzVMChefExtension</span></span>](./Remove-AzVMChefExtension.md)


