---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/revoke-azdiskaccess
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Revoke-AzDiskAccess.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Revoke-AzDiskAccess.md
ms.openlocfilehash: 76fb2e7483bb510d5eceb92b51f7e5e538c3b22b
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/27/2020
ms.locfileid: "94224570"
---
# <span data-ttu-id="ef75f-101">Revoke-AzDiskAccess</span><span class="sxs-lookup"><span data-stu-id="ef75f-101">Revoke-AzDiskAccess</span></span>

## <span data-ttu-id="ef75f-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="ef75f-102">SYNOPSIS</span></span>
<span data-ttu-id="ef75f-103">Odwołuje dostęp do dysku.</span><span class="sxs-lookup"><span data-stu-id="ef75f-103">Revokes an access to a disk.</span></span>

## <span data-ttu-id="ef75f-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="ef75f-104">SYNTAX</span></span>

```
Revoke-AzDiskAccess [-ResourceGroupName] <String> [-DiskName] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ef75f-105">Opis</span><span class="sxs-lookup"><span data-stu-id="ef75f-105">DESCRIPTION</span></span>
<span data-ttu-id="ef75f-106">Polecenie cmdlet **REVOKE-AzDiskAccess** odwołuje dostęp do dysku.</span><span class="sxs-lookup"><span data-stu-id="ef75f-106">The **Revoke-AzDiskAccess** cmdlet revokes an access to a disk.</span></span>

## <span data-ttu-id="ef75f-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="ef75f-107">EXAMPLES</span></span>

### <span data-ttu-id="ef75f-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="ef75f-108">Example 1</span></span>
```
PS C:\> Revoke-AzDiskAccess -ResourceGroupName 'ResourceGroup01' -DiskName 'Disk01'
```

<span data-ttu-id="ef75f-109">Odwoływanie dostępu do dysku o nazwie "Disk01" w grupie zasobów o nazwie "ResourceGroup01"</span><span class="sxs-lookup"><span data-stu-id="ef75f-109">Revoke the access to the disk named 'Disk01' in the resource group named 'ResourceGroup01'</span></span>

## <span data-ttu-id="ef75f-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="ef75f-110">PARAMETERS</span></span>

### <span data-ttu-id="ef75f-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ef75f-111">-AsJob</span></span>
<span data-ttu-id="ef75f-112">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="ef75f-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="ef75f-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ef75f-113">-DefaultProfile</span></span>
<span data-ttu-id="ef75f-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="ef75f-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ef75f-115">-Diskname</span><span class="sxs-lookup"><span data-stu-id="ef75f-115">-DiskName</span></span>
<span data-ttu-id="ef75f-116">Określa nazwę dysku.</span><span class="sxs-lookup"><span data-stu-id="ef75f-116">Specifies the name of a disk.</span></span>

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

### <span data-ttu-id="ef75f-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ef75f-117">-ResourceGroupName</span></span>
<span data-ttu-id="ef75f-118">Określa nazwę grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="ef75f-118">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="ef75f-119">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="ef75f-119">-Confirm</span></span>
<span data-ttu-id="ef75f-120">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ef75f-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ef75f-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ef75f-121">-WhatIf</span></span>
<span data-ttu-id="ef75f-122">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ef75f-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="ef75f-123">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="ef75f-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ef75f-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ef75f-124">CommonParameters</span></span>
<span data-ttu-id="ef75f-125">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ef75f-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ef75f-126">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ef75f-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ef75f-127">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ef75f-127">INPUTS</span></span>

### <span data-ttu-id="ef75f-128">System. String</span><span class="sxs-lookup"><span data-stu-id="ef75f-128">System.String</span></span>

## <span data-ttu-id="ef75f-129">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="ef75f-129">OUTPUTS</span></span>

### <span data-ttu-id="ef75f-130">Microsoft. Azure. Commands. COMPUTE. Automation. MODELES. PSOperationStatusResponse</span><span class="sxs-lookup"><span data-stu-id="ef75f-130">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="ef75f-131">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="ef75f-131">NOTES</span></span>

## <span data-ttu-id="ef75f-132">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="ef75f-132">RELATED LINKS</span></span>
