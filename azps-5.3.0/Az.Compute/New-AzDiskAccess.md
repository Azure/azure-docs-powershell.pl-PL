---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzDiskAccess.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzDiskAccess.md
ms.openlocfilehash: 430c0d09c56aa4fb57399c97714dc70cb19dd500
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98504087"
---
# <span data-ttu-id="6bc79-101">New-AzDiskAccess</span><span class="sxs-lookup"><span data-stu-id="6bc79-101">New-AzDiskAccess</span></span>

## <span data-ttu-id="6bc79-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="6bc79-102">SYNOPSIS</span></span>
<span data-ttu-id="6bc79-103">Tworzy zasób dostępu do dysku</span><span class="sxs-lookup"><span data-stu-id="6bc79-103">Creates a Disk Access resource</span></span>

## <span data-ttu-id="6bc79-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="6bc79-104">SYNTAX</span></span>

```
New-AzDiskAccess [-ResourceGroupName] <String> [-Name] <String> [-Location] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6bc79-105">Opis</span><span class="sxs-lookup"><span data-stu-id="6bc79-105">DESCRIPTION</span></span>
<span data-ttu-id="6bc79-106">Polecenie cmdlet **New-AzDiskAccess** tworzy zasób dostępu do dysku</span><span class="sxs-lookup"><span data-stu-id="6bc79-106">The **New-AzDiskAccess** cmdlet creates a Disk Access resource</span></span>

## <span data-ttu-id="6bc79-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="6bc79-107">EXAMPLES</span></span>

### <span data-ttu-id="6bc79-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="6bc79-108">Example 1</span></span>
```
PS C:\> New-AzDiskAccess -ResourceGroupName "ResourceGroup01" -Name "DiskAccess01" -Location "NorthCentralUS"
```

<span data-ttu-id="6bc79-109">To polecenie utworzy dostęp do dysku z podanymi właściwościami.</span><span class="sxs-lookup"><span data-stu-id="6bc79-109">This command will create a Disk Access with given properties.</span></span> 

## <span data-ttu-id="6bc79-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="6bc79-110">PARAMETERS</span></span>

### <span data-ttu-id="6bc79-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="6bc79-111">-AsJob</span></span>
<span data-ttu-id="6bc79-112">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="6bc79-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="6bc79-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6bc79-113">-DefaultProfile</span></span>
<span data-ttu-id="6bc79-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="6bc79-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6bc79-115">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="6bc79-115">-Location</span></span>
<span data-ttu-id="6bc79-116">Określa lokalizację.</span><span class="sxs-lookup"><span data-stu-id="6bc79-116">Specifies the location.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6bc79-117">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="6bc79-117">-Name</span></span>
<span data-ttu-id="6bc79-118">Określa nazwę dostępu do dysku.</span><span class="sxs-lookup"><span data-stu-id="6bc79-118">Specifies the name of a disk access.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: DiskAccessName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6bc79-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6bc79-119">-ResourceGroupName</span></span>
<span data-ttu-id="6bc79-120">Określa nazwę grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="6bc79-120">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="6bc79-121">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="6bc79-121">-Confirm</span></span>
<span data-ttu-id="6bc79-122">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6bc79-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6bc79-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6bc79-123">-WhatIf</span></span>
<span data-ttu-id="6bc79-124">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6bc79-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6bc79-125">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="6bc79-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6bc79-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6bc79-126">CommonParameters</span></span>
<span data-ttu-id="6bc79-127">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6bc79-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6bc79-128">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="6bc79-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6bc79-129">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="6bc79-129">INPUTS</span></span>

### <span data-ttu-id="6bc79-130">System. String</span><span class="sxs-lookup"><span data-stu-id="6bc79-130">System.String</span></span>

## <span data-ttu-id="6bc79-131">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="6bc79-131">OUTPUTS</span></span>

### <span data-ttu-id="6bc79-132">Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskAccess</span><span class="sxs-lookup"><span data-stu-id="6bc79-132">Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskAccess</span></span>

## <span data-ttu-id="6bc79-133">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="6bc79-133">NOTES</span></span>

## <span data-ttu-id="6bc79-134">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="6bc79-134">RELATED LINKS</span></span>
