---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: 473C71A8-1DF7-487A-B239-B80E2BB63B82
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRmVMChefExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRmVMChefExtension.md
ms.openlocfilehash: dc2e22acf8efd18a565c1ede7ff22aeb21679a47
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93544472"
---
# <span data-ttu-id="34e9f-101">Remove-AzureRmVMChefExtension</span><span class="sxs-lookup"><span data-stu-id="34e9f-101">Remove-AzureRmVMChefExtension</span></span>

## <span data-ttu-id="34e9f-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="34e9f-102">SYNOPSIS</span></span>
<span data-ttu-id="34e9f-103">Usuwa rozszerzenie Kuchmistrz z maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="34e9f-103">Removes the Chef extension from a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="34e9f-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="34e9f-104">SYNTAX</span></span>

### <span data-ttu-id="34e9f-105">Linux</span><span class="sxs-lookup"><span data-stu-id="34e9f-105">Linux</span></span>
```
Remove-AzureRmVMChefExtension [-ResourceGroupName] <String> [-VMName] <String> [[-Name] <String>] [-Linux]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="34e9f-106">Microsoft</span><span class="sxs-lookup"><span data-stu-id="34e9f-106">Windows</span></span>
```
Remove-AzureRmVMChefExtension [-ResourceGroupName] <String> [-VMName] <String> [[-Name] <String>] [-Windows]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="34e9f-107">Opis</span><span class="sxs-lookup"><span data-stu-id="34e9f-107">DESCRIPTION</span></span>
<span data-ttu-id="34e9f-108">Polecenie cmdlet **Remove-AzureVMChefExtension** usuwa rozszerzenie Kuchmistrz z maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="34e9f-108">The **Remove-AzureVMChefExtension** cmdlet removes the Chef extension from a virtual machine.</span></span>

## <span data-ttu-id="34e9f-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="34e9f-109">EXAMPLES</span></span>

### <span data-ttu-id="34e9f-110">Przykład 1: Usuwanie rozszerzenia Kuchmistrz z maszyny wirtualnej systemu Windows</span><span class="sxs-lookup"><span data-stu-id="34e9f-110">Example 1: Remove a Chef extension from a Windows virtual machine</span></span>
```
PS C:\> Remove-AzureRmVMChefExtension -ResourceGroupName "ResourceGroup001" -VMName "WindowsVM001" -Windows
```

<span data-ttu-id="34e9f-111">To polecenie usuwa rozszerzenie Kuchmistrz z maszyny wirtualnej opartej na systemie Windows o nazwie WindowsVM001 należącej do grupy zasobów o nazwie ResourceGroup001.</span><span class="sxs-lookup"><span data-stu-id="34e9f-111">This command removes a Chef extension from a Windows based virtual machine named WindowsVM001 that belongs to the resource group named ResourceGroup001.</span></span>

### <span data-ttu-id="34e9f-112">Przykład 2: Usuwanie rozszerzenia Kuchmistrz z maszyny wirtualnej Linux</span><span class="sxs-lookup"><span data-stu-id="34e9f-112">Example 2: Remove a Chef extension from a Linux virtual machine</span></span>
```
PS C:\> Remove-AzureRmVMChefExtension -ResourceGroupName "ResourceGroup002" -VMName "LinuxVM001" -Linux
```

<span data-ttu-id="34e9f-113">To polecenie usuwa rozszerzenie Kuchmistrz z maszyny wirtualnej opartej na systemie Linux o nazwie LinuxVM001 należącej do grupy zasobów o nazwie ResourceGroup002.</span><span class="sxs-lookup"><span data-stu-id="34e9f-113">This command removes a Chef extension from a Linux based virtual machine named LinuxVM001 that belongs to the resource group named ResourceGroup002.</span></span>

## <span data-ttu-id="34e9f-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="34e9f-114">PARAMETERS</span></span>

### <span data-ttu-id="34e9f-115">-Linux</span><span class="sxs-lookup"><span data-stu-id="34e9f-115">-Linux</span></span>
<span data-ttu-id="34e9f-116">Wskazuje, że to polecenie cmdlet ma element docelowy maszyny wirtualnej Linux.</span><span class="sxs-lookup"><span data-stu-id="34e9f-116">Indicates that this cmdlet targets a Linux virtual machine.</span></span>

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

### <span data-ttu-id="34e9f-117">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="34e9f-117">-Name</span></span>
<span data-ttu-id="34e9f-118">Określa nazwę rozszerzenia Kuchmistrz, które zostanie usunięte przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="34e9f-118">Specifies the name of the Chef extension that this cmdlet removes.</span></span>

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

### <span data-ttu-id="34e9f-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="34e9f-119">-ResourceGroupName</span></span>
<span data-ttu-id="34e9f-120">Określa nazwę grupy zasobów zawierającej maszynę wirtualną.</span><span class="sxs-lookup"><span data-stu-id="34e9f-120">Specifies the name of the resource group that contains the virtual machine.</span></span>

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

### <span data-ttu-id="34e9f-121">-VMName</span><span class="sxs-lookup"><span data-stu-id="34e9f-121">-VMName</span></span>
<span data-ttu-id="34e9f-122">Określa nazwę maszyny wirtualnej, dla której to polecenie cmdlet usuwa rozszerzenie Kuchmistrz.</span><span class="sxs-lookup"><span data-stu-id="34e9f-122">Specifies the name of a virtual machine for which this cmdlet removes the Chef extension.</span></span>

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

### <span data-ttu-id="34e9f-123">-Windows</span><span class="sxs-lookup"><span data-stu-id="34e9f-123">-Windows</span></span>
<span data-ttu-id="34e9f-124">Wskazuje, że to polecenie cmdlet ma element docelowy maszyny wirtualnej systemu Windows.</span><span class="sxs-lookup"><span data-stu-id="34e9f-124">Indicates that this cmdlet targets a Windows virtual machine.</span></span>

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

### <span data-ttu-id="34e9f-125">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="34e9f-125">-Confirm</span></span>
<span data-ttu-id="34e9f-126">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="34e9f-126">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="34e9f-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="34e9f-127">-WhatIf</span></span>
<span data-ttu-id="34e9f-128">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="34e9f-128">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="34e9f-129">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="34e9f-129">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="34e9f-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="34e9f-130">CommonParameters</span></span>
<span data-ttu-id="34e9f-131">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="34e9f-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="34e9f-132">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="34e9f-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="34e9f-133">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="34e9f-133">INPUTS</span></span>

### <span data-ttu-id="34e9f-134">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="34e9f-134">None</span></span>
<span data-ttu-id="34e9f-135">To polecenie cmdlet nie akceptuje żadnych danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="34e9f-135">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="34e9f-136">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="34e9f-136">OUTPUTS</span></span>

## <span data-ttu-id="34e9f-137">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="34e9f-137">NOTES</span></span>

## <span data-ttu-id="34e9f-138">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="34e9f-138">RELATED LINKS</span></span>

[<span data-ttu-id="34e9f-139">Get-AzureRmVMChefExtension</span><span class="sxs-lookup"><span data-stu-id="34e9f-139">Get-AzureRmVMChefExtension</span></span>](./Get-AzureRmVMChefExtension.md)

[<span data-ttu-id="34e9f-140">Set-AzureRmVMChefExtension</span><span class="sxs-lookup"><span data-stu-id="34e9f-140">Set-AzureRmVMChefExtension</span></span>](./Set-AzureRmVMChefExtension.md)
