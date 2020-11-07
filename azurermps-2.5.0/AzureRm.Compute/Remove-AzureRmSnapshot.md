---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/remove-azurermsnapshot
schema: 2.0.0
ms.openlocfilehash: cf63923b278f009cb676c79642882e64e6b8e303
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/15/2020
ms.locfileid: "93898950"
---
# <span data-ttu-id="9cdee-101">Remove-AzureRmSnapshot</span><span class="sxs-lookup"><span data-stu-id="9cdee-101">Remove-AzureRmSnapshot</span></span>

## <span data-ttu-id="9cdee-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="9cdee-102">SYNOPSIS</span></span>
<span data-ttu-id="9cdee-103">Usuwa migawkę.</span><span class="sxs-lookup"><span data-stu-id="9cdee-103">Removes a snapshot.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9cdee-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="9cdee-104">SYNTAX</span></span>

```
Remove-AzureRmSnapshot [-ResourceGroupName] <String> [-SnapshotName] <String> [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9cdee-105">Opis</span><span class="sxs-lookup"><span data-stu-id="9cdee-105">DESCRIPTION</span></span>
<span data-ttu-id="9cdee-106">Polecenie cmdlet **Remove-AzureRmSnapshot** umożliwia usunięcie migawki.</span><span class="sxs-lookup"><span data-stu-id="9cdee-106">The **Remove-AzureRmSnapshot** cmdlet removes a snapshot.</span></span>

## <span data-ttu-id="9cdee-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="9cdee-107">EXAMPLES</span></span>

### <span data-ttu-id="9cdee-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="9cdee-108">Example 1</span></span>
```
PS C:\> Remove-AzureRmSnapshot -ResourceGroupName 'ResourceGroup01' -SnapshotName 'Snapshot01' -Force;
```

<span data-ttu-id="9cdee-109">To polecenie usuwa migawkę o nazwie "Snapshot01" w grupie zasobów "ResourceGroup01".</span><span class="sxs-lookup"><span data-stu-id="9cdee-109">This command removes the snapshot named 'Snapshot01' in the resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="9cdee-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="9cdee-110">PARAMETERS</span></span>

### <span data-ttu-id="9cdee-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="9cdee-111">-AsJob</span></span>
<span data-ttu-id="9cdee-112">Uruchom polecenie cmdlet w tle i zwróć zadanie śledzenia postępu.</span><span class="sxs-lookup"><span data-stu-id="9cdee-112">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="9cdee-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9cdee-113">-DefaultProfile</span></span>
<span data-ttu-id="9cdee-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="9cdee-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9cdee-115">-Force</span><span class="sxs-lookup"><span data-stu-id="9cdee-115">-Force</span></span>
<span data-ttu-id="9cdee-116">Wymusza uruchomienie polecenia bez monitowania o potwierdzenie użytkownika.</span><span class="sxs-lookup"><span data-stu-id="9cdee-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="9cdee-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9cdee-117">-ResourceGroupName</span></span>
<span data-ttu-id="9cdee-118">Określa nazwę grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="9cdee-118">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="9cdee-119">-SnapshotName</span><span class="sxs-lookup"><span data-stu-id="9cdee-119">-SnapshotName</span></span>
<span data-ttu-id="9cdee-120">Określa nazwę migawki.</span><span class="sxs-lookup"><span data-stu-id="9cdee-120">Specifies the name of a snapshot.</span></span>

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

### <span data-ttu-id="9cdee-121">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="9cdee-121">-Confirm</span></span>
<span data-ttu-id="9cdee-122">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9cdee-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9cdee-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9cdee-123">-WhatIf</span></span>
<span data-ttu-id="9cdee-124">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9cdee-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9cdee-125">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="9cdee-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9cdee-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9cdee-126">CommonParameters</span></span>
<span data-ttu-id="9cdee-127">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9cdee-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9cdee-128">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9cdee-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9cdee-129">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="9cdee-129">INPUTS</span></span>

### <span data-ttu-id="9cdee-130">System. String</span><span class="sxs-lookup"><span data-stu-id="9cdee-130">System.String</span></span>

## <span data-ttu-id="9cdee-131">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="9cdee-131">OUTPUTS</span></span>

### <span data-ttu-id="9cdee-132">System. Object</span><span class="sxs-lookup"><span data-stu-id="9cdee-132">System.Object</span></span>

## <span data-ttu-id="9cdee-133">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="9cdee-133">NOTES</span></span>

## <span data-ttu-id="9cdee-134">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="9cdee-134">RELATED LINKS</span></span>

