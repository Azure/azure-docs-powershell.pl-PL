---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Revoke-AzureRmSnapshotAccess.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Revoke-AzureRmSnapshotAccess.md
ms.openlocfilehash: d081218a17bd5cac99256918d40ece722b73a85b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93718938"
---
# <span data-ttu-id="455b4-101">Revoke-AzureRmSnapshotAccess</span><span class="sxs-lookup"><span data-stu-id="455b4-101">Revoke-AzureRmSnapshotAccess</span></span>

## <span data-ttu-id="455b4-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="455b4-102">SYNOPSIS</span></span>
<span data-ttu-id="455b4-103">Odwołuje dostęp do migawki.</span><span class="sxs-lookup"><span data-stu-id="455b4-103">Revokes an access to a snapshot.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="455b4-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="455b4-104">SYNTAX</span></span>

```
Revoke-AzureRmSnapshotAccess [-ResourceGroupName] <String> [-SnapshotName] <String> [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="455b4-105">Opis</span><span class="sxs-lookup"><span data-stu-id="455b4-105">DESCRIPTION</span></span>
<span data-ttu-id="455b4-106">Polecenie cmdlet **REVOKE-AzureRmSnapshotAccess** odwołuje dostęp do migawki.</span><span class="sxs-lookup"><span data-stu-id="455b4-106">The **Revoke-AzureRmSnapshotAccess** cmdlet revokes an access to a snapshot.</span></span>

## <span data-ttu-id="455b4-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="455b4-107">EXAMPLES</span></span>

### <span data-ttu-id="455b4-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="455b4-108">Example 1</span></span>
```
PS C:\> Revoke-AzureRmDiskAccess -ResourceGroupName 'ResourceGroup01' -SnapshotName 'Snapshot01'
```

<span data-ttu-id="455b4-109">Odwoływanie dostępu do migawki o nazwie "Snapshot01" w grupie zasobów o nazwie "ResourceGroup01"</span><span class="sxs-lookup"><span data-stu-id="455b4-109">Revoke the access to the snapshot named 'Snapshot01' in the resource group named 'ResourceGroup01'</span></span>

## <span data-ttu-id="455b4-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="455b4-110">PARAMETERS</span></span>

### <span data-ttu-id="455b4-111">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="455b4-111">-ResourceGroupName</span></span>
<span data-ttu-id="455b4-112">Określa nazwę grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="455b4-112">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="455b4-113">-SnapshotName</span><span class="sxs-lookup"><span data-stu-id="455b4-113">-SnapshotName</span></span>
<span data-ttu-id="455b4-114">Określa nazwę migawki.</span><span class="sxs-lookup"><span data-stu-id="455b4-114">Specifies the name of a snapshot.</span></span>

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

### <span data-ttu-id="455b4-115">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="455b4-115">-Confirm</span></span>
<span data-ttu-id="455b4-116">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="455b4-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="455b4-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="455b4-117">-WhatIf</span></span>
<span data-ttu-id="455b4-118">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="455b4-118">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="455b4-119">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="455b4-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="455b4-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="455b4-120">CommonParameters</span></span>
<span data-ttu-id="455b4-121">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="455b4-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="455b4-122">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="455b4-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="455b4-123">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="455b4-123">INPUTS</span></span>

### <span data-ttu-id="455b4-124">System. String</span><span class="sxs-lookup"><span data-stu-id="455b4-124">System.String</span></span>

## <span data-ttu-id="455b4-125">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="455b4-125">OUTPUTS</span></span>

### <span data-ttu-id="455b4-126">System. Object</span><span class="sxs-lookup"><span data-stu-id="455b4-126">System.Object</span></span>

## <span data-ttu-id="455b4-127">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="455b4-127">NOTES</span></span>

## <span data-ttu-id="455b4-128">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="455b4-128">RELATED LINKS</span></span>

