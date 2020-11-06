---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRmDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRmDisk.md
ms.openlocfilehash: 10150d7941aa3b17a0a7d4447ff0a57e3d04a516
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93526934"
---
# <span data-ttu-id="584e5-101">Remove-AzureRmDisk</span><span class="sxs-lookup"><span data-stu-id="584e5-101">Remove-AzureRmDisk</span></span>

## <span data-ttu-id="584e5-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="584e5-102">SYNOPSIS</span></span>
<span data-ttu-id="584e5-103">Usuwa dysk.</span><span class="sxs-lookup"><span data-stu-id="584e5-103">Removes a disk.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="584e5-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="584e5-104">SYNTAX</span></span>

```
Remove-AzureRmDisk [-ResourceGroupName] <String> [-DiskName] <String> [-Force] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="584e5-105">Opis</span><span class="sxs-lookup"><span data-stu-id="584e5-105">DESCRIPTION</span></span>
<span data-ttu-id="584e5-106">Polecenie cmdlet **Remove-AzureRmDisk** usuwa dysk.</span><span class="sxs-lookup"><span data-stu-id="584e5-106">The **Remove-AzureRmDisk** cmdlet removes a disk.</span></span>

## <span data-ttu-id="584e5-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="584e5-107">EXAMPLES</span></span>

### <span data-ttu-id="584e5-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="584e5-108">Example 1</span></span>
```
PS C:\> Remove-AzureRmDisk -ResourceGroupName 'ResourceGroup01' -DiskName 'Disk01' -Force;
```

<span data-ttu-id="584e5-109">To polecenie usuwa dysk o nazwie "Disk01" w grupie zasobów "ResourceGroup01".</span><span class="sxs-lookup"><span data-stu-id="584e5-109">This command removes the disk named 'Disk01' in the resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="584e5-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="584e5-110">PARAMETERS</span></span>

### <span data-ttu-id="584e5-111">-Diskname</span><span class="sxs-lookup"><span data-stu-id="584e5-111">-DiskName</span></span>
<span data-ttu-id="584e5-112">Określa nazwę dysku.</span><span class="sxs-lookup"><span data-stu-id="584e5-112">Specifies the name of a disk.</span></span>

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

### <span data-ttu-id="584e5-113">-Force</span><span class="sxs-lookup"><span data-stu-id="584e5-113">-Force</span></span>
<span data-ttu-id="584e5-114">Wymusza uruchomienie polecenia bez monitowania o potwierdzenie użytkownika.</span><span class="sxs-lookup"><span data-stu-id="584e5-114">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="584e5-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="584e5-115">-ResourceGroupName</span></span>
<span data-ttu-id="584e5-116">Określa nazwę grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="584e5-116">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="584e5-117">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="584e5-117">-Confirm</span></span>
<span data-ttu-id="584e5-118">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="584e5-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="584e5-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="584e5-119">-WhatIf</span></span>
<span data-ttu-id="584e5-120">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="584e5-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="584e5-121">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="584e5-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="584e5-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="584e5-122">CommonParameters</span></span>
<span data-ttu-id="584e5-123">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="584e5-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="584e5-124">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="584e5-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="584e5-125">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="584e5-125">INPUTS</span></span>

### <span data-ttu-id="584e5-126">System. String</span><span class="sxs-lookup"><span data-stu-id="584e5-126">System.String</span></span>

## <span data-ttu-id="584e5-127">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="584e5-127">OUTPUTS</span></span>

### <span data-ttu-id="584e5-128">System. Object</span><span class="sxs-lookup"><span data-stu-id="584e5-128">System.Object</span></span>

## <span data-ttu-id="584e5-129">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="584e5-129">NOTES</span></span>

## <span data-ttu-id="584e5-130">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="584e5-130">RELATED LINKS</span></span>

