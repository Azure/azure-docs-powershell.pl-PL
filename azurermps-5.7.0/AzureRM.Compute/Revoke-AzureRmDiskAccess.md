---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Revoke-AzureRmDiskAccess.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Revoke-AzureRmDiskAccess.md
ms.openlocfilehash: 2b9573e3add842478977cf620873d3cf0cfdaa8f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93552991"
---
# <span data-ttu-id="39842-101">Revoke-AzureRmDiskAccess</span><span class="sxs-lookup"><span data-stu-id="39842-101">Revoke-AzureRmDiskAccess</span></span>

## <span data-ttu-id="39842-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="39842-102">SYNOPSIS</span></span>
<span data-ttu-id="39842-103">Odwołuje dostęp do dysku.</span><span class="sxs-lookup"><span data-stu-id="39842-103">Revokes an access to a disk.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="39842-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="39842-104">SYNTAX</span></span>

```
Revoke-AzureRmDiskAccess [-ResourceGroupName] <String> [-DiskName] <String> [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="39842-105">Opis</span><span class="sxs-lookup"><span data-stu-id="39842-105">DESCRIPTION</span></span>
<span data-ttu-id="39842-106">Polecenie cmdlet **REVOKE-AzureRmDiskAccess** odwołuje dostęp do dysku.</span><span class="sxs-lookup"><span data-stu-id="39842-106">The **Revoke-AzureRmDiskAccess** cmdlet revokes an access to a disk.</span></span>

## <span data-ttu-id="39842-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="39842-107">EXAMPLES</span></span>

### <span data-ttu-id="39842-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="39842-108">Example 1</span></span>
```
PS C:\> Revoke-AzureRmDiskAccess -ResourceGroupName 'ResourceGroup01' -DiskName 'Disk01'
```

<span data-ttu-id="39842-109">Odwoływanie dostępu do dysku o nazwie "Disk01" w grupie zasobów o nazwie "ResourceGroup01"</span><span class="sxs-lookup"><span data-stu-id="39842-109">Revoke the access to the disk named 'Disk01' in the resource group named 'ResourceGroup01'</span></span>

## <span data-ttu-id="39842-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="39842-110">PARAMETERS</span></span>

### <span data-ttu-id="39842-111">-Diskname</span><span class="sxs-lookup"><span data-stu-id="39842-111">-DiskName</span></span>
<span data-ttu-id="39842-112">Określa nazwę dysku.</span><span class="sxs-lookup"><span data-stu-id="39842-112">Specifies the name of a disk.</span></span>

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

### <span data-ttu-id="39842-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="39842-113">-ResourceGroupName</span></span>
<span data-ttu-id="39842-114">Określa nazwę grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="39842-114">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="39842-115">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="39842-115">-Confirm</span></span>
<span data-ttu-id="39842-116">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="39842-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="39842-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="39842-117">-WhatIf</span></span>
<span data-ttu-id="39842-118">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="39842-118">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="39842-119">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="39842-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="39842-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="39842-120">CommonParameters</span></span>
<span data-ttu-id="39842-121">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="39842-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="39842-122">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="39842-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="39842-123">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="39842-123">INPUTS</span></span>

### <span data-ttu-id="39842-124">System. String</span><span class="sxs-lookup"><span data-stu-id="39842-124">System.String</span></span>

## <span data-ttu-id="39842-125">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="39842-125">OUTPUTS</span></span>

### <span data-ttu-id="39842-126">System. Object</span><span class="sxs-lookup"><span data-stu-id="39842-126">System.Object</span></span>

## <span data-ttu-id="39842-127">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="39842-127">NOTES</span></span>

## <span data-ttu-id="39842-128">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="39842-128">RELATED LINKS</span></span>

