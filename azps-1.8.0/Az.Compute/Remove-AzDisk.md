---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azdisk
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzDisk.md
ms.openlocfilehash: 39e86ed1bf0a14bc0c7796ea9d8515be95c3a4ae
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93710255"
---
# <span data-ttu-id="335ef-101">Remove-AzDisk</span><span class="sxs-lookup"><span data-stu-id="335ef-101">Remove-AzDisk</span></span>

## <span data-ttu-id="335ef-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="335ef-102">SYNOPSIS</span></span>
<span data-ttu-id="335ef-103">Usuwa dysk.</span><span class="sxs-lookup"><span data-stu-id="335ef-103">Removes a disk.</span></span>

## <span data-ttu-id="335ef-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="335ef-104">SYNTAX</span></span>

```
Remove-AzDisk [-ResourceGroupName] <String> [-DiskName] <String> [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="335ef-105">Opis</span><span class="sxs-lookup"><span data-stu-id="335ef-105">DESCRIPTION</span></span>
<span data-ttu-id="335ef-106">Polecenie cmdlet **Remove-AzDisk** usuwa dysk.</span><span class="sxs-lookup"><span data-stu-id="335ef-106">The **Remove-AzDisk** cmdlet removes a disk.</span></span>

## <span data-ttu-id="335ef-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="335ef-107">EXAMPLES</span></span>

### <span data-ttu-id="335ef-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="335ef-108">Example 1</span></span>
```
PS C:\> Remove-AzDisk -ResourceGroupName 'ResourceGroup01' -DiskName 'Disk01' -Force;
```

<span data-ttu-id="335ef-109">To polecenie usuwa dysk o nazwie "Disk01" w grupie zasobów "ResourceGroup01".</span><span class="sxs-lookup"><span data-stu-id="335ef-109">This command removes the disk named 'Disk01' in the resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="335ef-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="335ef-110">PARAMETERS</span></span>

### <span data-ttu-id="335ef-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="335ef-111">-AsJob</span></span>
<span data-ttu-id="335ef-112">Uruchom polecenie cmdlet w tle i zwróć zadanie śledzenia postępu.</span><span class="sxs-lookup"><span data-stu-id="335ef-112">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="335ef-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="335ef-113">-DefaultProfile</span></span>
<span data-ttu-id="335ef-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="335ef-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="335ef-115">-Diskname</span><span class="sxs-lookup"><span data-stu-id="335ef-115">-DiskName</span></span>
<span data-ttu-id="335ef-116">Określa nazwę dysku.</span><span class="sxs-lookup"><span data-stu-id="335ef-116">Specifies the name of a disk.</span></span>

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

### <span data-ttu-id="335ef-117">-Force</span><span class="sxs-lookup"><span data-stu-id="335ef-117">-Force</span></span>
<span data-ttu-id="335ef-118">Wymusza uruchomienie polecenia bez monitowania o potwierdzenie użytkownika.</span><span class="sxs-lookup"><span data-stu-id="335ef-118">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="335ef-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="335ef-119">-ResourceGroupName</span></span>
<span data-ttu-id="335ef-120">Określa nazwę grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="335ef-120">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="335ef-121">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="335ef-121">-Confirm</span></span>
<span data-ttu-id="335ef-122">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="335ef-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="335ef-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="335ef-123">-WhatIf</span></span>
<span data-ttu-id="335ef-124">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="335ef-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="335ef-125">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="335ef-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="335ef-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="335ef-126">CommonParameters</span></span>
<span data-ttu-id="335ef-127">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="335ef-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="335ef-128">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="335ef-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="335ef-129">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="335ef-129">INPUTS</span></span>

### <span data-ttu-id="335ef-130">System. String</span><span class="sxs-lookup"><span data-stu-id="335ef-130">System.String</span></span>

## <span data-ttu-id="335ef-131">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="335ef-131">OUTPUTS</span></span>

### <span data-ttu-id="335ef-132">Microsoft. Azure. Commands. COMPUTE. Automation. MODELES. PSOperationStatusResponse</span><span class="sxs-lookup"><span data-stu-id="335ef-132">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="335ef-133">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="335ef-133">NOTES</span></span>

## <span data-ttu-id="335ef-134">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="335ef-134">RELATED LINKS</span></span>
