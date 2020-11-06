---
external help file: AzureRM.Compute.ManagedService-help.xml
Module Name: AzureRM.Compute.ManagedService
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute.managedservice/convertto-azurermvhd
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute.ManagedService/Commands.Compute.ManagedService/help/ConvertTo-AzureRmVhd.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute.ManagedService/Commands.Compute.ManagedService/help/ConvertTo-AzureRmVhd.md
ms.openlocfilehash: 0fa0f2d5cb78fe96f05b818b5cbfdabca47cbdee
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93526258"
---
# <span data-ttu-id="b5b1a-101">ConvertTo-AzureRmVhd</span><span class="sxs-lookup"><span data-stu-id="b5b1a-101">ConvertTo-AzureRmVhd</span></span>

## <span data-ttu-id="b5b1a-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="b5b1a-102">SYNOPSIS</span></span>
<span data-ttu-id="b5b1a-103">Konwertowanie maszyny wirtualnej funkcji Hyper-V na pliki wirtualnych dysków twardych obsługiwanych przez platformę Azure</span><span class="sxs-lookup"><span data-stu-id="b5b1a-103">Convert Hyper-V VM to Azure supported virtual hard disk files</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b5b1a-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="b5b1a-104">SYNTAX</span></span>

```
ConvertTo-AzureRmVhd -HyperVVMName <String> -ExportPath <String> [-HyperVServer <String>] [-Force] [-AsJob]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b5b1a-105">Opis</span><span class="sxs-lookup"><span data-stu-id="b5b1a-105">DESCRIPTION</span></span>
<span data-ttu-id="b5b1a-106">Konwertowanie maszyny wirtualnej funkcji Hyper-V na pliki wirtualnych dysków twardych obsługiwanych przez platformę Azure</span><span class="sxs-lookup"><span data-stu-id="b5b1a-106">Convert Hyper-V VM to Azure supported virtual hard disk files</span></span>

## <span data-ttu-id="b5b1a-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="b5b1a-107">EXAMPLES</span></span>

### <span data-ttu-id="b5b1a-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="b5b1a-108">Example 1</span></span>
```
PS C:\> ConvertTo-AzureRmVhd -HyperVVMName 'test' -ExportPath '.';
.\test\Virtual Hard Disks\Converted\os.vhd
.\test\Virtual Hard Disks\Converted\disk.vhd
```

<span data-ttu-id="b5b1a-109">Przekonwertuj MASZYNę wirtualną funkcji Hyper-V na nazwę test na pliki wirtualnych dysków twardych obsługiwane przez platformę Azure do bieżącego folderu.</span><span class="sxs-lookup"><span data-stu-id="b5b1a-109">Convert Hyper-V VM named 'test' to Azure supported virtual hard disk files to the current folder.</span></span>

## <span data-ttu-id="b5b1a-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="b5b1a-110">PARAMETERS</span></span>

### <span data-ttu-id="b5b1a-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b5b1a-111">-AsJob</span></span>
<span data-ttu-id="b5b1a-112">Uruchom polecenie cmdlet w tle i zwróć zadanie śledzenia postępu.</span><span class="sxs-lookup"><span data-stu-id="b5b1a-112">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="b5b1a-113">-ExportPath</span><span class="sxs-lookup"><span data-stu-id="b5b1a-113">-ExportPath</span></span>
<span data-ttu-id="b5b1a-114">Ścieżka folderu eksportu, która będzie zawierać pliki dysków.</span><span class="sxs-lookup"><span data-stu-id="b5b1a-114">The export folder path that will contain the disk files.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b5b1a-115">-Force</span><span class="sxs-lookup"><span data-stu-id="b5b1a-115">-Force</span></span>
<span data-ttu-id="b5b1a-116">Wymuś eksport nawet wtedy, gdy istniejący folder zostanie znaleziony.</span><span class="sxs-lookup"><span data-stu-id="b5b1a-116">Force the export even if existing folder is found.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b5b1a-117">-HyperVServer</span><span class="sxs-lookup"><span data-stu-id="b5b1a-117">-HyperVServer</span></span>
<span data-ttu-id="b5b1a-118">Nazwa DNS serwera funkcji Hyper-V z wartością domyślną "localhost".</span><span class="sxs-lookup"><span data-stu-id="b5b1a-118">The Hyper-V server DNS name, with 'localhost' as the default value.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: Localhost
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b5b1a-119">-HyperVVMName</span><span class="sxs-lookup"><span data-stu-id="b5b1a-119">-HyperVVMName</span></span>
<span data-ttu-id="b5b1a-120">Nazwa nazwy funkcji Hyper-V.</span><span class="sxs-lookup"><span data-stu-id="b5b1a-120">The Hyper-V name name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b5b1a-121">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="b5b1a-121">-Confirm</span></span>
<span data-ttu-id="b5b1a-122">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b5b1a-122">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b5b1a-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b5b1a-123">-WhatIf</span></span>
<span data-ttu-id="b5b1a-124">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b5b1a-124">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="b5b1a-125">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="b5b1a-125">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b5b1a-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b5b1a-126">CommonParameters</span></span>
<span data-ttu-id="b5b1a-127">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b5b1a-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b5b1a-128">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b5b1a-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b5b1a-129">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b5b1a-129">INPUTS</span></span>

### <span data-ttu-id="b5b1a-130">System. String</span><span class="sxs-lookup"><span data-stu-id="b5b1a-130">System.String</span></span>

## <span data-ttu-id="b5b1a-131">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="b5b1a-131">OUTPUTS</span></span>

### <span data-ttu-id="b5b1a-132">System. Management. Automation. PathInfo</span><span class="sxs-lookup"><span data-stu-id="b5b1a-132">System.Management.Automation.PathInfo</span></span>

## <span data-ttu-id="b5b1a-133">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="b5b1a-133">NOTES</span></span>

## <span data-ttu-id="b5b1a-134">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="b5b1a-134">RELATED LINKS</span></span>
