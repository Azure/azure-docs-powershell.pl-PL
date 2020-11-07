---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azdisk
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzDisk.md
ms.openlocfilehash: 46cbb87d54d1eb80857d3d0fbc786cb8296f4ac0
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93706297"
---
# <span data-ttu-id="08615-101">Remove-AzDisk</span><span class="sxs-lookup"><span data-stu-id="08615-101">Remove-AzDisk</span></span>

## <span data-ttu-id="08615-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="08615-102">SYNOPSIS</span></span>
<span data-ttu-id="08615-103">Usuwa dysk.</span><span class="sxs-lookup"><span data-stu-id="08615-103">Removes a disk.</span></span>

## <span data-ttu-id="08615-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="08615-104">SYNTAX</span></span>

```
Remove-AzDisk [-ResourceGroupName] <String> [-DiskName] <String> [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="08615-105">Opis</span><span class="sxs-lookup"><span data-stu-id="08615-105">DESCRIPTION</span></span>
<span data-ttu-id="08615-106">Polecenie cmdlet **Remove-AzDisk** usuwa dysk.</span><span class="sxs-lookup"><span data-stu-id="08615-106">The **Remove-AzDisk** cmdlet removes a disk.</span></span>

## <span data-ttu-id="08615-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="08615-107">EXAMPLES</span></span>

### <span data-ttu-id="08615-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="08615-108">Example 1</span></span>
```
PS C:\> Remove-AzDisk -ResourceGroupName 'ResourceGroup01' -DiskName 'Disk01' -Force;
```

<span data-ttu-id="08615-109">To polecenie usuwa dysk o nazwie "Disk01" w grupie zasobów "ResourceGroup01".</span><span class="sxs-lookup"><span data-stu-id="08615-109">This command removes the disk named 'Disk01' in the resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="08615-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="08615-110">PARAMETERS</span></span>

### <span data-ttu-id="08615-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="08615-111">-AsJob</span></span>
<span data-ttu-id="08615-112">Uruchom polecenie cmdlet w tle i zwróć zadanie śledzenia postępu.</span><span class="sxs-lookup"><span data-stu-id="08615-112">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="08615-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="08615-113">-DefaultProfile</span></span>
<span data-ttu-id="08615-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="08615-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="08615-115">-Diskname</span><span class="sxs-lookup"><span data-stu-id="08615-115">-DiskName</span></span>
<span data-ttu-id="08615-116">Określa nazwę dysku.</span><span class="sxs-lookup"><span data-stu-id="08615-116">Specifies the name of a disk.</span></span>

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

### <span data-ttu-id="08615-117">-Force</span><span class="sxs-lookup"><span data-stu-id="08615-117">-Force</span></span>
<span data-ttu-id="08615-118">Wymusza uruchomienie polecenia bez monitowania o potwierdzenie użytkownika.</span><span class="sxs-lookup"><span data-stu-id="08615-118">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="08615-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="08615-119">-ResourceGroupName</span></span>
<span data-ttu-id="08615-120">Określa nazwę grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="08615-120">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="08615-121">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="08615-121">-Confirm</span></span>
<span data-ttu-id="08615-122">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="08615-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="08615-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="08615-123">-WhatIf</span></span>
<span data-ttu-id="08615-124">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="08615-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="08615-125">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="08615-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="08615-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="08615-126">CommonParameters</span></span>
<span data-ttu-id="08615-127">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="08615-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="08615-128">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="08615-128">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="08615-129">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="08615-129">INPUTS</span></span>

### <span data-ttu-id="08615-130">System. String</span><span class="sxs-lookup"><span data-stu-id="08615-130">System.String</span></span>

## <span data-ttu-id="08615-131">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="08615-131">OUTPUTS</span></span>

### <span data-ttu-id="08615-132">Microsoft. Azure. Commands. COMPUTE. Automation. MODELES. PSOperationStatusResponse</span><span class="sxs-lookup"><span data-stu-id="08615-132">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="08615-133">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="08615-133">NOTES</span></span>

## <span data-ttu-id="08615-134">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="08615-134">RELATED LINKS</span></span>
