---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 5A2072B4-1533-46A2-9841-5509A44DE695
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/set-azsqldatabasegeobackuppolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlDatabaseGeoBackupPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlDatabaseGeoBackupPolicy.md
ms.openlocfilehash: 6ac39ae2daba5f97b9046f3860eb34d3bb0f03ce
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93887262"
---
# <span data-ttu-id="d2c1d-101">Set-AzSqlDatabaseGeoBackupPolicy</span><span class="sxs-lookup"><span data-stu-id="d2c1d-101">Set-AzSqlDatabaseGeoBackupPolicy</span></span>

## <span data-ttu-id="d2c1d-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="d2c1d-102">SYNOPSIS</span></span>
<span data-ttu-id="d2c1d-103">Ustawianie zasad tworzenia kopii zapasowej bazy danych.</span><span class="sxs-lookup"><span data-stu-id="d2c1d-103">Sets a database geo backup policy.</span></span>

## <span data-ttu-id="d2c1d-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="d2c1d-104">SYNTAX</span></span>

```
Set-AzSqlDatabaseGeoBackupPolicy -State <GeoBackupPolicyState> [-ServerName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="d2c1d-105">Opis</span><span class="sxs-lookup"><span data-stu-id="d2c1d-105">DESCRIPTION</span></span>
<span data-ttu-id="d2c1d-106">Polecenie cmdlet **Set-AzSqlDatabaseGeoBackupPolicy** ustawia zasady kopii zapasowej Geo zarejestrowane w bazie danych.</span><span class="sxs-lookup"><span data-stu-id="d2c1d-106">The **Set-AzSqlDatabaseGeoBackupPolicy** cmdlet sets the geo backup policy registered to a database.</span></span>
<span data-ttu-id="d2c1d-107">To jest zasób kopii zapasowej Azure służący do definiowania zasad magazynu kopii zapasowej.</span><span class="sxs-lookup"><span data-stu-id="d2c1d-107">This is an Azure Backup resource that is used to define backup storage policy.</span></span>

## <span data-ttu-id="d2c1d-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="d2c1d-108">EXAMPLES</span></span>

## <span data-ttu-id="d2c1d-109">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="d2c1d-109">PARAMETERS</span></span>

### <span data-ttu-id="d2c1d-110">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="d2c1d-110">-DatabaseName</span></span>
<span data-ttu-id="d2c1d-111">Określa nazwę bazy danych, dla której to polecenie cmdlet ustawia zasady tworzenia kopii zapasowych geograficznej.</span><span class="sxs-lookup"><span data-stu-id="d2c1d-111">Specifies the name of the database for which this cmdlet sets the geo backup policy.</span></span>

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

### <span data-ttu-id="d2c1d-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d2c1d-112">-DefaultProfile</span></span>
<span data-ttu-id="d2c1d-113">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="d2c1d-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d2c1d-114">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d2c1d-114">-ResourceGroupName</span></span>
<span data-ttu-id="d2c1d-115">Określa nazwę grupy zasobów serwera, która zawiera tę bazę danych.</span><span class="sxs-lookup"><span data-stu-id="d2c1d-115">Specifies the name of the resource group of the server that contains this database.</span></span>

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

### <span data-ttu-id="d2c1d-116">-Nazwa_serwera</span><span class="sxs-lookup"><span data-stu-id="d2c1d-116">-ServerName</span></span>
<span data-ttu-id="d2c1d-117">Określa nazwę serwera, na którym jest przechowywana baza danych.</span><span class="sxs-lookup"><span data-stu-id="d2c1d-117">Specifies the name of the server that hosts the database.</span></span>

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

### <span data-ttu-id="d2c1d-118">-State</span><span class="sxs-lookup"><span data-stu-id="d2c1d-118">-State</span></span>
<span data-ttu-id="d2c1d-119">Określa stan zasad tworzenia kopii zapasowej geograficznej.</span><span class="sxs-lookup"><span data-stu-id="d2c1d-119">Specifies the state of the geo backup policy.</span></span>
<span data-ttu-id="d2c1d-120">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="d2c1d-120">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="d2c1d-121">Wyłączona</span><span class="sxs-lookup"><span data-stu-id="d2c1d-121">Enabled</span></span> 
- <span data-ttu-id="d2c1d-122">Łącza</span><span class="sxs-lookup"><span data-stu-id="d2c1d-122">Disabled</span></span>

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

### <span data-ttu-id="d2c1d-123">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="d2c1d-123">-Confirm</span></span>
<span data-ttu-id="d2c1d-124">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d2c1d-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d2c1d-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d2c1d-125">-WhatIf</span></span>
<span data-ttu-id="d2c1d-126">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d2c1d-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d2c1d-127">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="d2c1d-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d2c1d-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d2c1d-128">CommonParameters</span></span>
<span data-ttu-id="d2c1d-129">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d2c1d-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d2c1d-130">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d2c1d-130">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d2c1d-131">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d2c1d-131">INPUTS</span></span>

### <span data-ttu-id="d2c1d-132">System. String</span><span class="sxs-lookup"><span data-stu-id="d2c1d-132">System.String</span></span>

## <span data-ttu-id="d2c1d-133">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="d2c1d-133">OUTPUTS</span></span>

### <span data-ttu-id="d2c1d-134">Microsoft. Azure. Commands. SQL. Backup. model. AzureSqlDatabaseGeoBackupPolicyModel</span><span class="sxs-lookup"><span data-stu-id="d2c1d-134">Microsoft.Azure.Commands.Sql.Backup.Model.AzureSqlDatabaseGeoBackupPolicyModel</span></span>

## <span data-ttu-id="d2c1d-135">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="d2c1d-135">NOTES</span></span>

## <span data-ttu-id="d2c1d-136">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="d2c1d-136">RELATED LINKS</span></span>

[<span data-ttu-id="d2c1d-137">Get-AzSqlDatabaseGeoBackupPolicy</span><span class="sxs-lookup"><span data-stu-id="d2c1d-137">Get-AzSqlDatabaseGeoBackupPolicy</span></span>](./Get-AzSqlDatabaseGeoBackupPolicy.md)

[<span data-ttu-id="d2c1d-138">Dokumentacja bazy danych SQL</span><span class="sxs-lookup"><span data-stu-id="d2c1d-138">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)

