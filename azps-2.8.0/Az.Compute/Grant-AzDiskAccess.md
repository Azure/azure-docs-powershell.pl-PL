---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/grant-azdiskaccess
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Grant-AzDiskAccess.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Grant-AzDiskAccess.md
ms.openlocfilehash: 6ff6784bda6bfd9052caa66d04f3f12bc11f568c
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93706370"
---
# <span data-ttu-id="f7271-101">Grant-AzDiskAccess</span><span class="sxs-lookup"><span data-stu-id="f7271-101">Grant-AzDiskAccess</span></span>

## <span data-ttu-id="f7271-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="f7271-102">SYNOPSIS</span></span>
<span data-ttu-id="f7271-103">Udziela dostępu do dysku.</span><span class="sxs-lookup"><span data-stu-id="f7271-103">Grants an access to a disk.</span></span>

## <span data-ttu-id="f7271-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="f7271-104">SYNTAX</span></span>

```
Grant-AzDiskAccess [-ResourceGroupName] <String> [-DiskName] <String> [-Access] <String>
 [[-DurationInSecond] <Int32>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="f7271-105">Opis</span><span class="sxs-lookup"><span data-stu-id="f7271-105">DESCRIPTION</span></span>
<span data-ttu-id="f7271-106">Polecenie cmdlet **Grant-AzDiskAccess** umożliwia uzyskanie dostępu do dysku.</span><span class="sxs-lookup"><span data-stu-id="f7271-106">The **Grant-AzDiskAccess** cmdlet grants an access to a disk.</span></span>

## <span data-ttu-id="f7271-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="f7271-107">EXAMPLES</span></span>

### <span data-ttu-id="f7271-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="f7271-108">Example 1</span></span>
```
PS C:\> Grant-AzDiskAccess -ResourceGroupName 'ResourceGroup01' -DiskName 'Disk01' -Access 'Read' -DurationInSecond 60;
```

<span data-ttu-id="f7271-109">Udziel uprawnienia "Odczyt" na dysk o nazwie "Disk01" w grupie zasobów o nazwie "ResourceGroup01" dla 60 sekund.</span><span class="sxs-lookup"><span data-stu-id="f7271-109">Grant 'Read' access to the disk named 'Disk01' in the resource group named 'ResourceGroup01' for 60 seconds.</span></span>

## <span data-ttu-id="f7271-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="f7271-110">PARAMETERS</span></span>

### <span data-ttu-id="f7271-111">— Dostęp</span><span class="sxs-lookup"><span data-stu-id="f7271-111">-Access</span></span>
<span data-ttu-id="f7271-112">Określa poziom dostępu.</span><span class="sxs-lookup"><span data-stu-id="f7271-112">Specifies Access level.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f7271-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f7271-113">-AsJob</span></span>
<span data-ttu-id="f7271-114">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="f7271-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="f7271-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f7271-115">-DefaultProfile</span></span>
<span data-ttu-id="f7271-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="f7271-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f7271-117">-Diskname</span><span class="sxs-lookup"><span data-stu-id="f7271-117">-DiskName</span></span>
<span data-ttu-id="f7271-118">Określa nazwę dysku.</span><span class="sxs-lookup"><span data-stu-id="f7271-118">Specifies the name of a disk.</span></span>

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

### <span data-ttu-id="f7271-119">-DurationInSecond</span><span class="sxs-lookup"><span data-stu-id="f7271-119">-DurationInSecond</span></span>
<span data-ttu-id="f7271-120">Określa czas trwania dostępu w sekundach.</span><span class="sxs-lookup"><span data-stu-id="f7271-120">Specifies access duration in seconds.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f7271-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f7271-121">-ResourceGroupName</span></span>
<span data-ttu-id="f7271-122">Określa nazwę grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="f7271-122">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="f7271-123">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="f7271-123">-Confirm</span></span>
<span data-ttu-id="f7271-124">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f7271-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f7271-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f7271-125">-WhatIf</span></span>
<span data-ttu-id="f7271-126">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f7271-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="f7271-127">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="f7271-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f7271-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f7271-128">CommonParameters</span></span>
<span data-ttu-id="f7271-129">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f7271-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f7271-130">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f7271-130">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f7271-131">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f7271-131">INPUTS</span></span>

### <span data-ttu-id="f7271-132">System. String</span><span class="sxs-lookup"><span data-stu-id="f7271-132">System.String</span></span>

## <span data-ttu-id="f7271-133">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="f7271-133">OUTPUTS</span></span>

### <span data-ttu-id="f7271-134">Microsoft. Azure. Commands. COMPUTE. Automation. MODELES. PSAccessUri</span><span class="sxs-lookup"><span data-stu-id="f7271-134">Microsoft.Azure.Commands.Compute.Automation.Models.PSAccessUri</span></span>

## <span data-ttu-id="f7271-135">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="f7271-135">NOTES</span></span>

## <span data-ttu-id="f7271-136">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="f7271-136">RELATED LINKS</span></span>