---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azsnapshot
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzSnapshot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzSnapshot.md
ms.openlocfilehash: 1b1ea7500974b37eb69dac1d2874cabc46b899b4
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93710251"
---
# <span data-ttu-id="e80c9-101">Remove-AzSnapshot</span><span class="sxs-lookup"><span data-stu-id="e80c9-101">Remove-AzSnapshot</span></span>

## <span data-ttu-id="e80c9-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="e80c9-102">SYNOPSIS</span></span>
<span data-ttu-id="e80c9-103">Usuwa migawkę.</span><span class="sxs-lookup"><span data-stu-id="e80c9-103">Removes a snapshot.</span></span>

## <span data-ttu-id="e80c9-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="e80c9-104">SYNTAX</span></span>

```
Remove-AzSnapshot [-ResourceGroupName] <String> [-SnapshotName] <String> [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e80c9-105">Opis</span><span class="sxs-lookup"><span data-stu-id="e80c9-105">DESCRIPTION</span></span>
<span data-ttu-id="e80c9-106">Polecenie cmdlet **Remove-AzSnapshot** umożliwia usunięcie migawki.</span><span class="sxs-lookup"><span data-stu-id="e80c9-106">The **Remove-AzSnapshot** cmdlet removes a snapshot.</span></span>

## <span data-ttu-id="e80c9-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="e80c9-107">EXAMPLES</span></span>

### <span data-ttu-id="e80c9-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="e80c9-108">Example 1</span></span>
```
PS C:\> Remove-AzSnapshot -ResourceGroupName 'ResourceGroup01' -SnapshotName 'Snapshot01' -Force;
```

<span data-ttu-id="e80c9-109">To polecenie usuwa migawkę o nazwie "Snapshot01" w grupie zasobów "ResourceGroup01".</span><span class="sxs-lookup"><span data-stu-id="e80c9-109">This command removes the snapshot named 'Snapshot01' in the resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="e80c9-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="e80c9-110">PARAMETERS</span></span>

### <span data-ttu-id="e80c9-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e80c9-111">-AsJob</span></span>
<span data-ttu-id="e80c9-112">Uruchom polecenie cmdlet w tle i zwróć zadanie śledzenia postępu.</span><span class="sxs-lookup"><span data-stu-id="e80c9-112">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="e80c9-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e80c9-113">-DefaultProfile</span></span>
<span data-ttu-id="e80c9-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="e80c9-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e80c9-115">-Force</span><span class="sxs-lookup"><span data-stu-id="e80c9-115">-Force</span></span>
<span data-ttu-id="e80c9-116">Wymusza uruchomienie polecenia bez monitowania o potwierdzenie użytkownika.</span><span class="sxs-lookup"><span data-stu-id="e80c9-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="e80c9-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e80c9-117">-ResourceGroupName</span></span>
<span data-ttu-id="e80c9-118">Określa nazwę grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="e80c9-118">Specifies the name of a resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e80c9-119">-SnapshotName</span><span class="sxs-lookup"><span data-stu-id="e80c9-119">-SnapshotName</span></span>
<span data-ttu-id="e80c9-120">Określa nazwę migawki.</span><span class="sxs-lookup"><span data-stu-id="e80c9-120">Specifies the name of a snapshot.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e80c9-121">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="e80c9-121">-Confirm</span></span>
<span data-ttu-id="e80c9-122">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e80c9-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e80c9-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e80c9-123">-WhatIf</span></span>
<span data-ttu-id="e80c9-124">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e80c9-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e80c9-125">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="e80c9-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e80c9-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e80c9-126">CommonParameters</span></span>
<span data-ttu-id="e80c9-127">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e80c9-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e80c9-128">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e80c9-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e80c9-129">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e80c9-129">INPUTS</span></span>

### <span data-ttu-id="e80c9-130">System. String</span><span class="sxs-lookup"><span data-stu-id="e80c9-130">System.String</span></span>

## <span data-ttu-id="e80c9-131">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="e80c9-131">OUTPUTS</span></span>

### <span data-ttu-id="e80c9-132">Microsoft. Azure. Commands. COMPUTE. Automation. MODELES. PSOperationStatusResponse</span><span class="sxs-lookup"><span data-stu-id="e80c9-132">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="e80c9-133">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="e80c9-133">NOTES</span></span>

## <span data-ttu-id="e80c9-134">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="e80c9-134">RELATED LINKS</span></span>
