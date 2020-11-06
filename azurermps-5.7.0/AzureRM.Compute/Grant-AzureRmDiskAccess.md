---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Grant-AzureRmDiskAccess.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Grant-AzureRmDiskAccess.md
ms.openlocfilehash: 2787c1cf8a37fd5d143e95c55d3e98b625d4d82e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93526953"
---
# <span data-ttu-id="d57c0-101">Grant-AzureRmDiskAccess</span><span class="sxs-lookup"><span data-stu-id="d57c0-101">Grant-AzureRmDiskAccess</span></span>

## <span data-ttu-id="d57c0-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="d57c0-102">SYNOPSIS</span></span>
<span data-ttu-id="d57c0-103">Udziela dostępu do dysku.</span><span class="sxs-lookup"><span data-stu-id="d57c0-103">Grants an access to a disk.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d57c0-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="d57c0-104">SYNTAX</span></span>

```
Grant-AzureRmDiskAccess [-ResourceGroupName] <String> [-DiskName] <String> [[-Access] <AccessLevel>]
 [[-DurationInSecond] <Int32>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d57c0-105">Opis</span><span class="sxs-lookup"><span data-stu-id="d57c0-105">DESCRIPTION</span></span>
<span data-ttu-id="d57c0-106">Polecenie cmdlet **Grant-AzureRmDiskAccess** umożliwia uzyskanie dostępu do dysku.</span><span class="sxs-lookup"><span data-stu-id="d57c0-106">The **Grant-AzureRmDiskAccess** cmdlet grants an access to a disk.</span></span>

## <span data-ttu-id="d57c0-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="d57c0-107">EXAMPLES</span></span>

### <span data-ttu-id="d57c0-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="d57c0-108">Example 1</span></span>
```
PS C:\> Grant-AzureRmDiskAccess -ResourceGroupName 'ResourceGroup01' -DiskName 'Disk01' -Access 'Read' -DurationInSecond 60;
```

<span data-ttu-id="d57c0-109">Udziel uprawnienia "Odczyt" na dysk o nazwie "Disk01" w grupie zasobów o nazwie "ResourceGroup01" dla 60 sekund.</span><span class="sxs-lookup"><span data-stu-id="d57c0-109">Grant 'Read' access to the disk named 'Disk01' in the resource group named 'ResourceGroup01' for 60 seconds.</span></span>

## <span data-ttu-id="d57c0-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="d57c0-110">PARAMETERS</span></span>

### <span data-ttu-id="d57c0-111">— Dostęp</span><span class="sxs-lookup"><span data-stu-id="d57c0-111">-Access</span></span>
<span data-ttu-id="d57c0-112">Określa poziom dostępu.</span><span class="sxs-lookup"><span data-stu-id="d57c0-112">Specifies Access level.</span></span>

```yaml
Type: AccessLevel
Parameter Sets: (All)
Aliases: 
Accepted values: None, Read

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d57c0-113">-Diskname</span><span class="sxs-lookup"><span data-stu-id="d57c0-113">-DiskName</span></span>
<span data-ttu-id="d57c0-114">Określa nazwę dysku.</span><span class="sxs-lookup"><span data-stu-id="d57c0-114">Specifies the name of a disk.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d57c0-115">-DurationInSecond</span><span class="sxs-lookup"><span data-stu-id="d57c0-115">-DurationInSecond</span></span>
<span data-ttu-id="d57c0-116">Określa czas trwania dostępu w sekundach.</span><span class="sxs-lookup"><span data-stu-id="d57c0-116">Specifies access duration in seconds.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d57c0-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d57c0-117">-ResourceGroupName</span></span>
<span data-ttu-id="d57c0-118">Określa nazwę grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="d57c0-118">Specifies the name of a resource group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d57c0-119">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="d57c0-119">-Confirm</span></span>
<span data-ttu-id="d57c0-120">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d57c0-120">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d57c0-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d57c0-121">-WhatIf</span></span>
<span data-ttu-id="d57c0-122">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d57c0-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="d57c0-123">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="d57c0-123">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d57c0-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d57c0-124">CommonParameters</span></span>
<span data-ttu-id="d57c0-125">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d57c0-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d57c0-126">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d57c0-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d57c0-127">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d57c0-127">INPUTS</span></span>

### <span data-ttu-id="d57c0-128">System. String</span><span class="sxs-lookup"><span data-stu-id="d57c0-128">System.String</span></span>

## <span data-ttu-id="d57c0-129">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="d57c0-129">OUTPUTS</span></span>

### <span data-ttu-id="d57c0-130">System. Object</span><span class="sxs-lookup"><span data-stu-id="d57c0-130">System.Object</span></span>

## <span data-ttu-id="d57c0-131">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="d57c0-131">NOTES</span></span>

## <span data-ttu-id="d57c0-132">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="d57c0-132">RELATED LINKS</span></span>

