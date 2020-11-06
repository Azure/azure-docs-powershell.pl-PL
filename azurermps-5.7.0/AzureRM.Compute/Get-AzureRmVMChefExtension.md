---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: F41953F1-9515-4081-8624-6A1494DA4BB2
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmVMChefExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmVMChefExtension.md
ms.openlocfilehash: 5733939c24437c974f629588106d6240766a9df1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93544515"
---
# <span data-ttu-id="760f5-101">Get-AzureRmVMChefExtension</span><span class="sxs-lookup"><span data-stu-id="760f5-101">Get-AzureRmVMChefExtension</span></span>

## <span data-ttu-id="760f5-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="760f5-102">SYNOPSIS</span></span>
<span data-ttu-id="760f5-103">Pobiera informacje o rozszerzeniu Kuchmistrz.</span><span class="sxs-lookup"><span data-stu-id="760f5-103">Gets information about a Chef extension.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="760f5-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="760f5-104">SYNTAX</span></span>

### <span data-ttu-id="760f5-105">Linux</span><span class="sxs-lookup"><span data-stu-id="760f5-105">Linux</span></span>
```
Get-AzureRmVMChefExtension [-ResourceGroupName] <String> [-VMName] <String> [[-Name] <String>] [-Status]
 [-Linux] [<CommonParameters>]
```

### <span data-ttu-id="760f5-106">Microsoft</span><span class="sxs-lookup"><span data-stu-id="760f5-106">Windows</span></span>
```
Get-AzureRmVMChefExtension [-ResourceGroupName] <String> [-VMName] <String> [[-Name] <String>] [-Status]
 [-Windows] [<CommonParameters>]
```

## <span data-ttu-id="760f5-107">Opis</span><span class="sxs-lookup"><span data-stu-id="760f5-107">DESCRIPTION</span></span>
<span data-ttu-id="760f5-108">Polecenie cmdlet **Get-AzureVMChefExtension** pobiera informacje o rozszerzeniu Kuchmistrz zainstalowanym na maszynie wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="760f5-108">The **Get-AzureVMChefExtension** cmdlet gets information about a Chef extension installed on a virtual machine.</span></span>

## <span data-ttu-id="760f5-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="760f5-109">EXAMPLES</span></span>

### <span data-ttu-id="760f5-110">Przykład 1: uzyskiwanie szczegółowych informacji o rozszerzeniu Kuchmistrz dla maszyny wirtualnej systemu Windows</span><span class="sxs-lookup"><span data-stu-id="760f5-110">Example 1: Get the details of Chef extension for a Windows virtual machine-</span></span>
```
PS C:\> Get-AzureRmVMChefExtension -ResourceGroupName "ResourceGroup001" -VMName "WindowsVM001" -Windows
```

<span data-ttu-id="760f5-111">To polecenie pobiera rozszerzenie Kuchmistrz z maszyny wirtualnej systemu Windows o nazwie WindowsVM001 należącej do grupy zasobów o nazwie ResourceGroup001.</span><span class="sxs-lookup"><span data-stu-id="760f5-111">This command gets the Chef extension from a Windows virtual machine named WindowsVM001 that belongs to the resource group named ResourceGroup001.</span></span>

### <span data-ttu-id="760f5-112">Przykład 2: uzyskiwanie szczegółowych informacji o rozszerzeniu Kuchmistrz dla maszyny wirtualnej Linux</span><span class="sxs-lookup"><span data-stu-id="760f5-112">Example 2: Get the details of Chef extension for a Linux virtual machine</span></span>
```
PS C:\> Get-AzureRmVMChefExtension -ResourceGroupName "ResourceGroup002" -VMName "LinuxVM001" -Linux
```

<span data-ttu-id="760f5-113">To polecenie pobiera rozszerzenie Kuchmistrz z maszyny wirtualnej Linux o nazwie LinuxVM001 należącej do grupy zasobów o nazwie ResourceGroup002.</span><span class="sxs-lookup"><span data-stu-id="760f5-113">This command gets the Chef extension from a Linux virtual machine named LinuxVM001 that belongs to the resource group named ResourceGroup002.</span></span>

## <span data-ttu-id="760f5-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="760f5-114">PARAMETERS</span></span>

### <span data-ttu-id="760f5-115">-Linux</span><span class="sxs-lookup"><span data-stu-id="760f5-115">-Linux</span></span>
<span data-ttu-id="760f5-116">Wskazuje, że to polecenie cmdlet działa na maszynie wirtualnej Linux.</span><span class="sxs-lookup"><span data-stu-id="760f5-116">Indicates that this cmdlet works on a Linux virtual machine.</span></span>

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

### <span data-ttu-id="760f5-117">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="760f5-117">-Name</span></span>
<span data-ttu-id="760f5-118">Określa nazwę rozszerzenia Kuchmistrz.</span><span class="sxs-lookup"><span data-stu-id="760f5-118">Specifies the name of the Chef extension.</span></span>

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

### <span data-ttu-id="760f5-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="760f5-119">-ResourceGroupName</span></span>
<span data-ttu-id="760f5-120">Określa nazwę grupy zasobów zawierającej maszynę wirtualną.</span><span class="sxs-lookup"><span data-stu-id="760f5-120">Specifies the name of the resource group that contains the virtual machine.</span></span>

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

### <span data-ttu-id="760f5-121">-Status</span><span class="sxs-lookup"><span data-stu-id="760f5-121">-Status</span></span>
<span data-ttu-id="760f5-122">Wskazuje, że to polecenie cmdlet pobiera tylko widok wystąpienia rozszerzenia Kuchmistrz.</span><span class="sxs-lookup"><span data-stu-id="760f5-122">Indicates that this cmdlet gets only the instance view of the Chef extension.</span></span>

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

### <span data-ttu-id="760f5-123">-VMName</span><span class="sxs-lookup"><span data-stu-id="760f5-123">-VMName</span></span>
<span data-ttu-id="760f5-124">Określa nazwę maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="760f5-124">Specifies the name of a virtual machine.</span></span>

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

### <span data-ttu-id="760f5-125">-Windows</span><span class="sxs-lookup"><span data-stu-id="760f5-125">-Windows</span></span>
<span data-ttu-id="760f5-126">Wskazuje, że to polecenie cmdlet dotyczy maszyny wirtualnej systemu Windows.</span><span class="sxs-lookup"><span data-stu-id="760f5-126">Indicates that this cmdlet is for a Windows virtual machine.</span></span>

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

### <span data-ttu-id="760f5-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="760f5-127">CommonParameters</span></span>
<span data-ttu-id="760f5-128">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="760f5-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="760f5-129">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="760f5-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="760f5-130">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="760f5-130">INPUTS</span></span>

### <span data-ttu-id="760f5-131">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="760f5-131">None</span></span>
<span data-ttu-id="760f5-132">To polecenie cmdlet nie akceptuje żadnych danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="760f5-132">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="760f5-133">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="760f5-133">OUTPUTS</span></span>

## <span data-ttu-id="760f5-134">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="760f5-134">NOTES</span></span>

## <span data-ttu-id="760f5-135">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="760f5-135">RELATED LINKS</span></span>

[<span data-ttu-id="760f5-136">Set-AzureRmVMChefExtension</span><span class="sxs-lookup"><span data-stu-id="760f5-136">Set-AzureRmVMChefExtension</span></span>](./Set-AzureRmVMChefExtension.md)

[<span data-ttu-id="760f5-137">Remove-AzureRmVMChefExtension</span><span class="sxs-lookup"><span data-stu-id="760f5-137">Remove-AzureRmVMChefExtension</span></span>](./Remove-AzureRmVMChefExtension.md)


