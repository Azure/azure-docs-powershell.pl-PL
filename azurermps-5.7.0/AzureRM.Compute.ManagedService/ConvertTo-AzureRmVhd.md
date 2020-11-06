---
external help file: ''
Module Name: ''
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute.managedservice/convertto-azurermvhd
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute.ManagedService/Commands.Compute.ManagedService/help/ConvertTo-AzureRmVhd.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute.ManagedService/Commands.Compute.ManagedService/help/ConvertTo-AzureRmVhd.md
ms.openlocfilehash: c440fa43a4e15abb5ab9f87d5b814fe3cbc55d63
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93542736"
---
# <span data-ttu-id="07bd9-101">ConvertTo-AzureRmVhd</span><span class="sxs-lookup"><span data-stu-id="07bd9-101">ConvertTo-AzureRmVhd</span></span>

## <span data-ttu-id="07bd9-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="07bd9-102">SYNOPSIS</span></span>
<span data-ttu-id="07bd9-103">Konwertowanie maszyny wirtualnej funkcji Hyper-V na pliki wirtualnych dysków twardych obsługiwanych przez platformę Azure</span><span class="sxs-lookup"><span data-stu-id="07bd9-103">Convert Hyper-V VM to Azure supported virtual hard disk files</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="07bd9-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="07bd9-104">SYNTAX</span></span>

```
ConvertTo-AzureRmVhd -HyperVVMName <String> -ExportPath <String> [-HyperVServer <String>] [-Force] [-AsJob]
 [<CommonParameters>]
```

## <span data-ttu-id="07bd9-105">Opis</span><span class="sxs-lookup"><span data-stu-id="07bd9-105">DESCRIPTION</span></span>
<span data-ttu-id="07bd9-106">Konwertowanie maszyny wirtualnej funkcji Hyper-V na pliki wirtualnych dysków twardych obsługiwanych przez platformę Azure</span><span class="sxs-lookup"><span data-stu-id="07bd9-106">Convert Hyper-V VM to Azure supported virtual hard disk files</span></span>

## <span data-ttu-id="07bd9-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="07bd9-107">EXAMPLES</span></span>

### <span data-ttu-id="07bd9-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="07bd9-108">Example 1</span></span>
```
PS C:\> ConvertTo-AzureRmVhd -HyperVVMName 'test' -ExportPath '.';
.\test\Virtual Hard Disks\Converted\os.vhd
.\test\Virtual Hard Disks\Converted\disk.vhd
```

<span data-ttu-id="07bd9-109">Przekonwertuj MASZYNę wirtualną funkcji Hyper-V na nazwę test na pliki wirtualnych dysków twardych obsługiwane przez platformę Azure do bieżącego folderu.</span><span class="sxs-lookup"><span data-stu-id="07bd9-109">Convert Hyper-V VM named 'test' to Azure supported virtual hard disk files to the current folder.</span></span>

## <span data-ttu-id="07bd9-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="07bd9-110">PARAMETERS</span></span>

### <span data-ttu-id="07bd9-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="07bd9-111">-AsJob</span></span>
<span data-ttu-id="07bd9-112">Uruchom polecenie cmdlet w tle i zwróć zadanie śledzenia postępu.</span><span class="sxs-lookup"><span data-stu-id="07bd9-112">Run cmdlet in the background and return a Job to track progress.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="07bd9-113">-ExportPath</span><span class="sxs-lookup"><span data-stu-id="07bd9-113">-ExportPath</span></span>
<span data-ttu-id="07bd9-114">Ścieżka folderu eksportu, która będzie zawierać pliki dysków.</span><span class="sxs-lookup"><span data-stu-id="07bd9-114">The export folder path that will contain the disk files.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="07bd9-115">-Force</span><span class="sxs-lookup"><span data-stu-id="07bd9-115">-Force</span></span>
<span data-ttu-id="07bd9-116">Wymuś eksport nawet wtedy, gdy istniejący folder zostanie znaleziony.</span><span class="sxs-lookup"><span data-stu-id="07bd9-116">Force the export even if existing folder is found.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="07bd9-117">-HyperVServer</span><span class="sxs-lookup"><span data-stu-id="07bd9-117">-HyperVServer</span></span>
<span data-ttu-id="07bd9-118">Nazwa DNS serwera funkcji Hyper-V z wartością domyślną "localhost".</span><span class="sxs-lookup"><span data-stu-id="07bd9-118">The Hyper-V server DNS name, with 'localhost' as the default value.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: Localhost
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="07bd9-119">-HyperVVMName</span><span class="sxs-lookup"><span data-stu-id="07bd9-119">-HyperVVMName</span></span>
<span data-ttu-id="07bd9-120">Nazwa nazwy funkcji Hyper-V.</span><span class="sxs-lookup"><span data-stu-id="07bd9-120">The Hyper-V name name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="07bd9-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="07bd9-121">CommonParameters</span></span>
<span data-ttu-id="07bd9-122">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="07bd9-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="07bd9-123">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="07bd9-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="07bd9-124">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="07bd9-124">INPUTS</span></span>

### <span data-ttu-id="07bd9-125">System. String</span><span class="sxs-lookup"><span data-stu-id="07bd9-125">System.String</span></span>

## <span data-ttu-id="07bd9-126">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="07bd9-126">OUTPUTS</span></span>

### <span data-ttu-id="07bd9-127">System. Management. Automation. PathInfo</span><span class="sxs-lookup"><span data-stu-id="07bd9-127">System.Management.Automation.PathInfo</span></span>

## <span data-ttu-id="07bd9-128">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="07bd9-128">NOTES</span></span>

## <span data-ttu-id="07bd9-129">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="07bd9-129">RELATED LINKS</span></span>

