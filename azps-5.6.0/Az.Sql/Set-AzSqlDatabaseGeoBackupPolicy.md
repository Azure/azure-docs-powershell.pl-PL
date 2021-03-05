---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 5A2072B4-1533-46A2-9841-5509A44DE695
online version: https://docs.microsoft.com/powershell/module/az.sql/set-azsqldatabasegeobackuppolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlDatabaseGeoBackupPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlDatabaseGeoBackupPolicy.md
ms.openlocfilehash: 18ae68a4ecf0a2511f992e42a202468193022d6f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101994904"
---
# <span data-ttu-id="8bf78-101">Set-AzSqlDatabaseGeoBackupPolicy</span><span class="sxs-lookup"><span data-stu-id="8bf78-101">Set-AzSqlDatabaseGeoBackupPolicy</span></span>

## <span data-ttu-id="8bf78-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8bf78-102">SYNOPSIS</span></span>
<span data-ttu-id="8bf78-103">Ustawia zasady tworzenia kopii geograficznej bazy danych.</span><span class="sxs-lookup"><span data-stu-id="8bf78-103">Sets a database geo backup policy.</span></span>

## <span data-ttu-id="8bf78-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="8bf78-104">SYNTAX</span></span>

```
Set-AzSqlDatabaseGeoBackupPolicy -State <GeoBackupPolicyState> [-ServerName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="8bf78-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="8bf78-105">DESCRIPTION</span></span>
<span data-ttu-id="8bf78-106">Polecenie **cmdlet Set-AzSqlDatabaseGeoBackupPolicy** ustawia zasady tworzenia kopii zapasowej geolokalizacji zarejestrowane w bazie danych.</span><span class="sxs-lookup"><span data-stu-id="8bf78-106">The **Set-AzSqlDatabaseGeoBackupPolicy** cmdlet sets the geo backup policy registered to a database.</span></span>
<span data-ttu-id="8bf78-107">Jest to zasób usługi Azure Backup, który służy do definiowania zasad przechowywania kopii zapasowej.</span><span class="sxs-lookup"><span data-stu-id="8bf78-107">This is an Azure Backup resource that is used to define backup storage policy.</span></span>

## <span data-ttu-id="8bf78-108">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="8bf78-108">EXAMPLES</span></span>

## <span data-ttu-id="8bf78-109">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8bf78-109">PARAMETERS</span></span>

### <span data-ttu-id="8bf78-110">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="8bf78-110">-DatabaseName</span></span>
<span data-ttu-id="8bf78-111">Określa nazwę bazy danych, dla której to polecenie cmdlet ustawia zasady tworzenia kopii zapasowej geolokalizacji.</span><span class="sxs-lookup"><span data-stu-id="8bf78-111">Specifies the name of the database for which this cmdlet sets the geo backup policy.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8bf78-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8bf78-112">-DefaultProfile</span></span>
<span data-ttu-id="8bf78-113">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="8bf78-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="8bf78-114">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8bf78-114">-ResourceGroupName</span></span>
<span data-ttu-id="8bf78-115">Określa nazwę grupy zasobów serwera zawierającego tę bazę danych.</span><span class="sxs-lookup"><span data-stu-id="8bf78-115">Specifies the name of the resource group of the server that contains this database.</span></span>

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

### <span data-ttu-id="8bf78-116">-ServerName</span><span class="sxs-lookup"><span data-stu-id="8bf78-116">-ServerName</span></span>
<span data-ttu-id="8bf78-117">Określa nazwę serwera hostowego bazę danych.</span><span class="sxs-lookup"><span data-stu-id="8bf78-117">Specifies the name of the server that hosts the database.</span></span>

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

### <span data-ttu-id="8bf78-118">— województwo</span><span class="sxs-lookup"><span data-stu-id="8bf78-118">-State</span></span>
<span data-ttu-id="8bf78-119">Określa stan zasad tworzenia kopii zapasowej geolokalizacji.</span><span class="sxs-lookup"><span data-stu-id="8bf78-119">Specifies the state of the geo backup policy.</span></span>
<span data-ttu-id="8bf78-120">Dopuszczalne wartości dla tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="8bf78-120">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="8bf78-121">Włączone</span><span class="sxs-lookup"><span data-stu-id="8bf78-121">Enabled</span></span> 
- <span data-ttu-id="8bf78-122">Wyłączone</span><span class="sxs-lookup"><span data-stu-id="8bf78-122">Disabled</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.Backup.Model.AzureSqlDatabaseGeoBackupPolicyModel+GeoBackupPolicyState
Parameter Sets: (All)
Aliases:
Accepted values: Disabled, Enabled

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8bf78-123">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="8bf78-123">-Confirm</span></span>
<span data-ttu-id="8bf78-124">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="8bf78-124">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8bf78-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8bf78-125">-WhatIf</span></span>
<span data-ttu-id="8bf78-126">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8bf78-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8bf78-127">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="8bf78-127">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8bf78-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8bf78-128">CommonParameters</span></span>
<span data-ttu-id="8bf78-129">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8bf78-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8bf78-130">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="8bf78-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8bf78-131">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="8bf78-131">INPUTS</span></span>

### <span data-ttu-id="8bf78-132">System.String</span><span class="sxs-lookup"><span data-stu-id="8bf78-132">System.String</span></span>

## <span data-ttu-id="8bf78-133">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="8bf78-133">OUTPUTS</span></span>

### <span data-ttu-id="8bf78-134">Microsoft.Azure.Commands.Sql.Backup.Model.AzureSqlDatabaseGeoBackupPolicyModel</span><span class="sxs-lookup"><span data-stu-id="8bf78-134">Microsoft.Azure.Commands.Sql.Backup.Model.AzureSqlDatabaseGeoBackupPolicyModel</span></span>

## <span data-ttu-id="8bf78-135">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="8bf78-135">NOTES</span></span>

## <span data-ttu-id="8bf78-136">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="8bf78-136">RELATED LINKS</span></span>

[<span data-ttu-id="8bf78-137">Get-AzSqlDatabaseGeoBackupPolicy</span><span class="sxs-lookup"><span data-stu-id="8bf78-137">Get-AzSqlDatabaseGeoBackupPolicy</span></span>](./Get-AzSqlDatabaseGeoBackupPolicy.md)

[<span data-ttu-id="8bf78-138">Dokumentacja bazy danych SQL</span><span class="sxs-lookup"><span data-stu-id="8bf78-138">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)

