---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/powershell/module/az.synapse/get-azsynapsesqlpoolgeobackup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseSqlPoolGeoBackup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseSqlPoolGeoBackup.md
ms.openlocfilehash: d1c0b6439b148d51506861a6bfffc6a6681343ef
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101957866"
---
# <span data-ttu-id="bab89-101">Get-AzSynapseSqlPoolGeoBackup</span><span class="sxs-lookup"><span data-stu-id="bab89-101">Get-AzSynapseSqlPoolGeoBackup</span></span>

## <span data-ttu-id="bab89-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bab89-102">SYNOPSIS</span></span>
<span data-ttu-id="bab89-103">Pobiera nadmiarową geograficznie kopię zapasową puli sql.</span><span class="sxs-lookup"><span data-stu-id="bab89-103">Gets a geo-redundant backup of a Sql Pool.</span></span>

## <span data-ttu-id="bab89-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="bab89-104">SYNTAX</span></span>

### <span data-ttu-id="bab89-105">GetByNameParameterSet (domyślne)</span><span class="sxs-lookup"><span data-stu-id="bab89-105">GetByNameParameterSet (Default)</span></span>
```
Get-AzSynapseSqlPoolGeoBackup [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="bab89-106">SqlPoolGeoBackupResourceId</span><span class="sxs-lookup"><span data-stu-id="bab89-106">SqlPoolGeoBackupResourceId</span></span>
```
Get-AzSynapseSqlPoolGeoBackup [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="bab89-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="bab89-107">DESCRIPTION</span></span>
<span data-ttu-id="bab89-108">Polecenie **cmdlet Get-AzSynapseSqlPoolGeoBackup** pobiera określoną geograficznie nadmiarową kopię zapasową puli SQL lub wszystkie dostępne geograficznie nadmiarowe kopie zapasowe w określonym obszarze roboczym.</span><span class="sxs-lookup"><span data-stu-id="bab89-108">The **Get-AzSynapseSqlPoolGeoBackup** cmdlet gets a specified geo-redundant backup of a SQL Pool or all available geo-redundant backups on a specified workspace.</span></span>
<span data-ttu-id="bab89-109">Geograficznie nadmiarowa kopia zapasowa to zasób, który można przywrócić, używając plików danych z oddzielnej lokalizacji geograficznej.</span><span class="sxs-lookup"><span data-stu-id="bab89-109">A geo-redundant backup is a restorable resource using data files from a separate geographic location.</span></span>
<span data-ttu-id="bab89-110">Za pomocą Geo-Restore można przywrócić geograficznie nadmiarową kopię zapasową na wypadek 30-owej 32-65-855 0000 0000000000000000000000000000000000000000000000000000000</span><span class="sxs-lookup"><span data-stu-id="bab89-110">You can use Geo-Restore to restore a geo-redundant backup in the event of a regional outage to recover your Sql Pool to a new region.</span></span>

## <span data-ttu-id="bab89-111">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="bab89-111">EXAMPLES</span></span>

### <span data-ttu-id="bab89-112">Przykład 1. Uzyskiwanie określonej nadmiarowej geograficznej kopii zapasowej</span><span class="sxs-lookup"><span data-stu-id="bab89-112">Example 1: Get a specified geo-redundant backup</span></span>
```powershell
PS C:\> Get-AzSynapseSqlPoolGeoBackup -ResourceGroupName ContosoResourceGroup -WorkspaceName "ContosoWorkspace" -Name "ContosoSqlPool"
```
<span data-ttu-id="bab89-113">Polecenie cmdlet pobiera kopię zapasową lokalizacji geograficznej dla puli sql.</span><span class="sxs-lookup"><span data-stu-id="bab89-113">The cmdlet retrieves Geo Backup for a sql pool.</span></span>

### <span data-ttu-id="bab89-114">Przykład 2. Uzyskiwanie wszystkich nadmiarowych geograficznie kopii zapasowych w obszarze roboczym</span><span class="sxs-lookup"><span data-stu-id="bab89-114">Example 2: Get all geo-redundant backups on a workspace</span></span>
```
PS C:\>Get-AzSynapseSqlPoolGeoBackup -ResourceGroupName "ContosoResourceGroup" -WorkspaceName "ContosoWorkspace"
```
<span data-ttu-id="bab89-115">To polecenie pobiera wszystkie dostępne geograficznie nadmiarowe kopie zapasowe w określonym obszarze roboczym.</span><span class="sxs-lookup"><span data-stu-id="bab89-115">This command gets all available geo-redundant backups on a specified workspace.</span></span>

### <span data-ttu-id="bab89-116">Przykład 3. Uzyskiwanie wszystkich nadmiarowych geograficznie kopii zapasowych w obszarze roboczym przy użyciu filtrowania</span><span class="sxs-lookup"><span data-stu-id="bab89-116">Example 3: Get all geo-redundant backups on a workspace using filtering</span></span>
```
PS C:\>Get-AzSynapseSqlPoolGeoBackup -ResourceGroupName "ContosoResourceGroup" -WorkspaceName "ContosoWorkspace" -Name "Contoso*"
```
<span data-ttu-id="bab89-117">To polecenie pobiera wszystkie dostępne geograficznie nadmiarowe kopie zapasowe w określonym obszarze roboczym, które zaczynają się od "Contoso".</span><span class="sxs-lookup"><span data-stu-id="bab89-117">This command gets all available geo-redundant backups on a specified workspace that start with "Contoso".</span></span>

## <span data-ttu-id="bab89-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="bab89-118">PARAMETERS</span></span>

### <span data-ttu-id="bab89-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bab89-119">-DefaultProfile</span></span>
<span data-ttu-id="bab89-120">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="bab89-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bab89-121">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="bab89-121">-Name</span></span>
<span data-ttu-id="bab89-122">Pula języka Sql Synapse.</span><span class="sxs-lookup"><span data-stu-id="bab89-122">The Synapse Sql pool.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet
Aliases: The Synapse Sql pool.

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bab89-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="bab89-123">-ResourceId</span></span>
<span data-ttu-id="bab89-124">Wprowadź identyfikator zasobu geo kopii zapasowej puli sql.</span><span class="sxs-lookup"><span data-stu-id="bab89-124">Input a Sql Pool Geo Backup Resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: SqlPoolGeoBackupResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bab89-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bab89-125">-ResourceGroupName</span></span>
<span data-ttu-id="bab89-126">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="bab89-126">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bab89-127">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="bab89-127">-WorkspaceName</span></span>
<span data-ttu-id="bab89-128">Nazwa obszaru roboczego aplikacji Synapse.</span><span class="sxs-lookup"><span data-stu-id="bab89-128">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bab89-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bab89-129">CommonParameters</span></span>
<span data-ttu-id="bab89-130">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bab89-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bab89-131">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="bab89-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bab89-132">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="bab89-132">INPUTS</span></span>

### <span data-ttu-id="bab89-133">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="bab89-133">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="bab89-134">Microsoft.Azure.Commands.Synapse.Models.PSSynapseResourceGroup</span><span class="sxs-lookup"><span data-stu-id="bab89-134">Microsoft.Azure.Commands.Synapse.Models.PSSynapseResourceGroup</span></span>

## <span data-ttu-id="bab89-135">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="bab89-135">OUTPUTS</span></span>

### <span data-ttu-id="bab89-136">Microsoft.Azure.Commands.Synapse.Models.PSBackupModel</span><span class="sxs-lookup"><span data-stu-id="bab89-136">Microsoft.Azure.Commands.Synapse.Models.PSBackupModel</span></span>

## <span data-ttu-id="bab89-137">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="bab89-137">NOTES</span></span>

## <span data-ttu-id="bab89-138">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="bab89-138">RELATED LINKS</span></span>
