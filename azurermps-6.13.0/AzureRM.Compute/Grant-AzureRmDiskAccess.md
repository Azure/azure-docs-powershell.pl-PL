---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/grant-azurermdiskaccess
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Grant-AzureRmDiskAccess.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Grant-AzureRmDiskAccess.md
ms.openlocfilehash: ae45dadd2d5af2cf81a8735ca6725ee4798dbf29
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93548855"
---
# <span data-ttu-id="67704-101">Grant-AzureRmDiskAccess</span><span class="sxs-lookup"><span data-stu-id="67704-101">Grant-AzureRmDiskAccess</span></span>

## <span data-ttu-id="67704-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="67704-102">SYNOPSIS</span></span>
<span data-ttu-id="67704-103">Udziela dostępu do dysku.</span><span class="sxs-lookup"><span data-stu-id="67704-103">Grants an access to a disk.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="67704-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="67704-104">SYNTAX</span></span>

```
Grant-AzureRmDiskAccess [-ResourceGroupName] <String> [-DiskName] <String> [-Access] <String>
 [[-DurationInSecond] <Int32>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="67704-105">Opis</span><span class="sxs-lookup"><span data-stu-id="67704-105">DESCRIPTION</span></span>
<span data-ttu-id="67704-106">Polecenie cmdlet **Grant-AzureRmDiskAccess** umożliwia uzyskanie dostępu do dysku.</span><span class="sxs-lookup"><span data-stu-id="67704-106">The **Grant-AzureRmDiskAccess** cmdlet grants an access to a disk.</span></span>

## <span data-ttu-id="67704-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="67704-107">EXAMPLES</span></span>

### <span data-ttu-id="67704-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="67704-108">Example 1</span></span>
```
PS C:\> Grant-AzureRmDiskAccess -ResourceGroupName 'ResourceGroup01' -DiskName 'Disk01' -Access 'Read' -DurationInSecond 60;
```

<span data-ttu-id="67704-109">Udziel uprawnienia "Odczyt" na dysk o nazwie "Disk01" w grupie zasobów o nazwie "ResourceGroup01" dla 60 sekund.</span><span class="sxs-lookup"><span data-stu-id="67704-109">Grant 'Read' access to the disk named 'Disk01' in the resource group named 'ResourceGroup01' for 60 seconds.</span></span>

## <span data-ttu-id="67704-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="67704-110">PARAMETERS</span></span>

### <span data-ttu-id="67704-111">— Dostęp</span><span class="sxs-lookup"><span data-stu-id="67704-111">-Access</span></span>
<span data-ttu-id="67704-112">Określa poziom dostępu.</span><span class="sxs-lookup"><span data-stu-id="67704-112">Specifies Access level.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="67704-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="67704-113">-AsJob</span></span>
<span data-ttu-id="67704-114">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="67704-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="67704-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="67704-115">-DefaultProfile</span></span>
<span data-ttu-id="67704-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="67704-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="67704-117">-Diskname</span><span class="sxs-lookup"><span data-stu-id="67704-117">-DiskName</span></span>
<span data-ttu-id="67704-118">Określa nazwę dysku.</span><span class="sxs-lookup"><span data-stu-id="67704-118">Specifies the name of a disk.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="67704-119">-DurationInSecond</span><span class="sxs-lookup"><span data-stu-id="67704-119">-DurationInSecond</span></span>
<span data-ttu-id="67704-120">Określa czas trwania dostępu w sekundach.</span><span class="sxs-lookup"><span data-stu-id="67704-120">Specifies access duration in seconds.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="67704-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="67704-121">-ResourceGroupName</span></span>
<span data-ttu-id="67704-122">Określa nazwę grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="67704-122">Specifies the name of a resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="67704-123">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="67704-123">-Confirm</span></span>
<span data-ttu-id="67704-124">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="67704-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="67704-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="67704-125">-WhatIf</span></span>
<span data-ttu-id="67704-126">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="67704-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="67704-127">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="67704-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="67704-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="67704-128">CommonParameters</span></span>
<span data-ttu-id="67704-129">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="67704-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="67704-130">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="67704-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="67704-131">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="67704-131">INPUTS</span></span>

### <span data-ttu-id="67704-132">System. String</span><span class="sxs-lookup"><span data-stu-id="67704-132">System.String</span></span>

## <span data-ttu-id="67704-133">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="67704-133">OUTPUTS</span></span>

### <span data-ttu-id="67704-134">Microsoft. Azure. Commands. COMPUTE. Automation. MODELES. PSAccessUri</span><span class="sxs-lookup"><span data-stu-id="67704-134">Microsoft.Azure.Commands.Compute.Automation.Models.PSAccessUri</span></span>

## <span data-ttu-id="67704-135">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="67704-135">NOTES</span></span>

## <span data-ttu-id="67704-136">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="67704-136">RELATED LINKS</span></span>
