---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/get-aznetappfilessnapshotpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Get-AzNetAppFilesSnapshotPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Get-AzNetAppFilesSnapshotPolicy.md
ms.openlocfilehash: b65bfc61b354a5a45ac009b40b54de46d94ef56c
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98490010"
---
# <span data-ttu-id="1e452-101">Get-AzNetAppFilesSnapshotPolicy</span><span class="sxs-lookup"><span data-stu-id="1e452-101">Get-AzNetAppFilesSnapshotPolicy</span></span>

## <span data-ttu-id="1e452-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="1e452-102">SYNOPSIS</span></span>
<span data-ttu-id="1e452-103">Pobiera szczegóły dotyczące zasad migawki plików usługi Azure NetApp (ANF).</span><span class="sxs-lookup"><span data-stu-id="1e452-103">Gets details of an Azure NetApp Files (ANF) snapshot policy.</span></span>

## <span data-ttu-id="1e452-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="1e452-104">SYNTAX</span></span>

### <span data-ttu-id="1e452-105">ByFieldsParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="1e452-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzNetAppFilesSnapshotPolicy -ResourceGroupName <String> -AccountName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1e452-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="1e452-106">ByResourceIdParameterSet</span></span>
```
Get-AzNetAppFilesSnapshotPolicy -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1e452-107">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="1e452-107">ByParentObjectParameterSet</span></span>
```
Get-AzNetAppFilesSnapshotPolicy -AccountObject <PSNetAppFilesAccount>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1e452-108">Opis</span><span class="sxs-lookup"><span data-stu-id="1e452-108">DESCRIPTION</span></span>
<span data-ttu-id="1e452-109">Polecenie cmdlet **Get-AzNetAppFilesSnapshotPolicy** pobiera szczegółowe informacje o zasadach migawki ANF.</span><span class="sxs-lookup"><span data-stu-id="1e452-109">The **Get-AzNetAppFilesSnapshotPolicy** cmdlet gets details of an ANF snapshot policy.</span></span>

## <span data-ttu-id="1e452-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="1e452-110">EXAMPLES</span></span>

### <span data-ttu-id="1e452-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="1e452-111">Example 1</span></span>
```powershell
PS C:\> Get-AzNetAppFilesSnapshotPolicy -ResourceGroupName "MyRG" -AccountName "MyAnfAccount" -Name "MySnapshotPolicy"
```

<span data-ttu-id="1e452-112">To polecenie pobiera zasady tworzenia kopii zapasowych o nazwie "MyBackupPolicy" dla konta "MyAnfAccount".</span><span class="sxs-lookup"><span data-stu-id="1e452-112">This command gets the backup policy named "MyBackupPolicy" for account "MyAnfAccount".</span></span>

## <span data-ttu-id="1e452-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="1e452-113">PARAMETERS</span></span>

### <span data-ttu-id="1e452-114">-AccountName</span><span class="sxs-lookup"><span data-stu-id="1e452-114">-AccountName</span></span>
<span data-ttu-id="1e452-115">Nazwa konta usługi ANF</span><span class="sxs-lookup"><span data-stu-id="1e452-115">The name of the ANF account</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1e452-116">-Accountobject</span><span class="sxs-lookup"><span data-stu-id="1e452-116">-AccountObject</span></span>
<span data-ttu-id="1e452-117">Konto nowego obiektu zasad migawki</span><span class="sxs-lookup"><span data-stu-id="1e452-117">The Account for the new Snapshot Policy object</span></span>

```yaml
Type: Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount
Parameter Sets: ByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1e452-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1e452-118">-DefaultProfile</span></span>
<span data-ttu-id="1e452-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="1e452-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1e452-120">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="1e452-120">-Name</span></span>
<span data-ttu-id="1e452-121">Nazwa zasady migawki ANF</span><span class="sxs-lookup"><span data-stu-id="1e452-121">The name of the ANF snapshot policy</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases: SnapshotPolicyName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1e452-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1e452-122">-ResourceGroupName</span></span>
<span data-ttu-id="1e452-123">Grupa zasobów konta ANF</span><span class="sxs-lookup"><span data-stu-id="1e452-123">The resource group of the ANF account</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1e452-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="1e452-124">-ResourceId</span></span>
<span data-ttu-id="1e452-125">Identyfikator zasobu w zasadach migawki ANF</span><span class="sxs-lookup"><span data-stu-id="1e452-125">The resource id of the ANF Snapshot Policy</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1e452-126">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="1e452-126">-Confirm</span></span>
<span data-ttu-id="1e452-127">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1e452-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1e452-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1e452-128">-WhatIf</span></span>
<span data-ttu-id="1e452-129">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1e452-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1e452-130">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="1e452-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1e452-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1e452-131">CommonParameters</span></span>
<span data-ttu-id="1e452-132">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1e452-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1e452-133">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="1e452-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1e452-134">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="1e452-134">INPUTS</span></span>

### <span data-ttu-id="1e452-135">System. String</span><span class="sxs-lookup"><span data-stu-id="1e452-135">System.String</span></span>

### <span data-ttu-id="1e452-136">Microsoft. Azure. Commands. NetAppFiles. models. PSNetAppFilesAccount</span><span class="sxs-lookup"><span data-stu-id="1e452-136">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span></span>

## <span data-ttu-id="1e452-137">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="1e452-137">OUTPUTS</span></span>

### <span data-ttu-id="1e452-138">Microsoft. Azure. Commands. NetAppFiles. models. PSNetAppFilesSnapshotPolicy</span><span class="sxs-lookup"><span data-stu-id="1e452-138">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesSnapshotPolicy</span></span>

## <span data-ttu-id="1e452-139">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="1e452-139">NOTES</span></span>

## <span data-ttu-id="1e452-140">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="1e452-140">RELATED LINKS</span></span>
