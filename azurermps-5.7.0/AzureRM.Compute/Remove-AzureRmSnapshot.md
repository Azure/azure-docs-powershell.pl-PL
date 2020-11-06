---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRmSnapshot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRmSnapshot.md
ms.openlocfilehash: 36dec1f8d4374f2e5bbed1f742aa7733bb760f67
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93544480"
---
# <span data-ttu-id="74c12-101">Remove-AzureRmSnapshot</span><span class="sxs-lookup"><span data-stu-id="74c12-101">Remove-AzureRmSnapshot</span></span>

## <span data-ttu-id="74c12-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="74c12-102">SYNOPSIS</span></span>
<span data-ttu-id="74c12-103">Usuwa migawkę.</span><span class="sxs-lookup"><span data-stu-id="74c12-103">Removes a snapshot.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="74c12-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="74c12-104">SYNTAX</span></span>

```
Remove-AzureRmSnapshot [-ResourceGroupName] <String> [-SnapshotName] <String> [-Force] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="74c12-105">Opis</span><span class="sxs-lookup"><span data-stu-id="74c12-105">DESCRIPTION</span></span>
<span data-ttu-id="74c12-106">Polecenie cmdlet **Remove-AzureRmSnapshot** umożliwia usunięcie migawki.</span><span class="sxs-lookup"><span data-stu-id="74c12-106">The **Remove-AzureRmSnapshot** cmdlet removes a snapshot.</span></span>

## <span data-ttu-id="74c12-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="74c12-107">EXAMPLES</span></span>

### <span data-ttu-id="74c12-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="74c12-108">Example 1</span></span>
```
PS C:\> Remove-AzureRmSnapshot -ResourceGroupName 'ResourceGroup01' -SnapshotName 'Snapshot01' -Force;
```

<span data-ttu-id="74c12-109">To polecenie usuwa migawkę o nazwie "Snapshot01" w grupie zasobów "ResourceGroup01".</span><span class="sxs-lookup"><span data-stu-id="74c12-109">This command removes the snapshot named 'Snapshot01' in the resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="74c12-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="74c12-110">PARAMETERS</span></span>

### <span data-ttu-id="74c12-111">-Force</span><span class="sxs-lookup"><span data-stu-id="74c12-111">-Force</span></span>
<span data-ttu-id="74c12-112">Wymusza uruchomienie polecenia bez monitowania o potwierdzenie użytkownika.</span><span class="sxs-lookup"><span data-stu-id="74c12-112">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="74c12-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="74c12-113">-ResourceGroupName</span></span>
<span data-ttu-id="74c12-114">Określa nazwę grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="74c12-114">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="74c12-115">-SnapshotName</span><span class="sxs-lookup"><span data-stu-id="74c12-115">-SnapshotName</span></span>
<span data-ttu-id="74c12-116">Określa nazwę migawki.</span><span class="sxs-lookup"><span data-stu-id="74c12-116">Specifies the name of a snapshot.</span></span>

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

### <span data-ttu-id="74c12-117">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="74c12-117">-Confirm</span></span>
<span data-ttu-id="74c12-118">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="74c12-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="74c12-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="74c12-119">-WhatIf</span></span>
<span data-ttu-id="74c12-120">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="74c12-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="74c12-121">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="74c12-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="74c12-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="74c12-122">CommonParameters</span></span>
<span data-ttu-id="74c12-123">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="74c12-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="74c12-124">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="74c12-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="74c12-125">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="74c12-125">INPUTS</span></span>

### <span data-ttu-id="74c12-126">System. String</span><span class="sxs-lookup"><span data-stu-id="74c12-126">System.String</span></span>

## <span data-ttu-id="74c12-127">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="74c12-127">OUTPUTS</span></span>

### <span data-ttu-id="74c12-128">System. Object</span><span class="sxs-lookup"><span data-stu-id="74c12-128">System.Object</span></span>

## <span data-ttu-id="74c12-129">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="74c12-129">NOTES</span></span>

## <span data-ttu-id="74c12-130">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="74c12-130">RELATED LINKS</span></span>

