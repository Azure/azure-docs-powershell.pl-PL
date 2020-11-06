---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 5A2072B4-1533-46A2-9841-5509A44DE695
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/set-azurermsqldatabasegeobackuppolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlDatabaseGeoBackupPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlDatabaseGeoBackupPolicy.md
ms.openlocfilehash: c7aa097318f65cd2506ccfcd96e4d9eeeaf9d1bf
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93541439"
---
# <span data-ttu-id="7ca58-101">Set-AzureRmSqlDatabaseGeoBackupPolicy</span><span class="sxs-lookup"><span data-stu-id="7ca58-101">Set-AzureRmSqlDatabaseGeoBackupPolicy</span></span>

## <span data-ttu-id="7ca58-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="7ca58-102">SYNOPSIS</span></span>
<span data-ttu-id="7ca58-103">Ustawianie zasad tworzenia kopii zapasowej bazy danych.</span><span class="sxs-lookup"><span data-stu-id="7ca58-103">Sets a database geo backup policy.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7ca58-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="7ca58-104">SYNTAX</span></span>

```
Set-AzureRmSqlDatabaseGeoBackupPolicy -State <GeoBackupPolicyState> [-ServerName] <String>
 [-DatabaseName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7ca58-105">Opis</span><span class="sxs-lookup"><span data-stu-id="7ca58-105">DESCRIPTION</span></span>
<span data-ttu-id="7ca58-106">Polecenie cmdlet **Set-AzureRmSqlDatabaseGeoBackupPolicy** ustawia zasady kopii zapasowej Geo zarejestrowane w bazie danych.</span><span class="sxs-lookup"><span data-stu-id="7ca58-106">The **Set-AzureRmSqlDatabaseGeoBackupPolicy** cmdlet sets the geo backup policy registered to a database.</span></span>
<span data-ttu-id="7ca58-107">To jest zasób kopii zapasowej Azure służący do definiowania zasad magazynu kopii zapasowej.</span><span class="sxs-lookup"><span data-stu-id="7ca58-107">This is an Azure Backup resource that is used to define backup storage policy.</span></span>

## <span data-ttu-id="7ca58-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="7ca58-108">EXAMPLES</span></span>

## <span data-ttu-id="7ca58-109">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="7ca58-109">PARAMETERS</span></span>

### <span data-ttu-id="7ca58-110">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="7ca58-110">-DatabaseName</span></span>
<span data-ttu-id="7ca58-111">Określa nazwę bazy danych, dla której to polecenie cmdlet ustawia zasady tworzenia kopii zapasowych geograficznej.</span><span class="sxs-lookup"><span data-stu-id="7ca58-111">Specifies the name of the database for which this cmdlet sets the geo backup policy.</span></span>

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

### <span data-ttu-id="7ca58-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7ca58-112">-DefaultProfile</span></span>
<span data-ttu-id="7ca58-113">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="7ca58-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="7ca58-114">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7ca58-114">-ResourceGroupName</span></span>
<span data-ttu-id="7ca58-115">Określa nazwę grupy zasobów serwera, która zawiera tę bazę danych.</span><span class="sxs-lookup"><span data-stu-id="7ca58-115">Specifies the name of the resource group of the server that contains this database.</span></span>

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

### <span data-ttu-id="7ca58-116">-Nazwa_serwera</span><span class="sxs-lookup"><span data-stu-id="7ca58-116">-ServerName</span></span>
<span data-ttu-id="7ca58-117">Określa nazwę serwera, na którym jest przechowywana baza danych.</span><span class="sxs-lookup"><span data-stu-id="7ca58-117">Specifies the name of the server that hosts the database.</span></span>

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

### <span data-ttu-id="7ca58-118">-State</span><span class="sxs-lookup"><span data-stu-id="7ca58-118">-State</span></span>
<span data-ttu-id="7ca58-119">Określa stan zasad tworzenia kopii zapasowej geograficznej.</span><span class="sxs-lookup"><span data-stu-id="7ca58-119">Specifies the state of the geo backup policy.</span></span>
<span data-ttu-id="7ca58-120">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="7ca58-120">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="7ca58-121">Wyłączona</span><span class="sxs-lookup"><span data-stu-id="7ca58-121">Enabled</span></span> 
- <span data-ttu-id="7ca58-122">Łącza</span><span class="sxs-lookup"><span data-stu-id="7ca58-122">Disabled</span></span>

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

### <span data-ttu-id="7ca58-123">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="7ca58-123">-Confirm</span></span>
<span data-ttu-id="7ca58-124">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7ca58-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7ca58-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7ca58-125">-WhatIf</span></span>
<span data-ttu-id="7ca58-126">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7ca58-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7ca58-127">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="7ca58-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7ca58-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7ca58-128">CommonParameters</span></span>
<span data-ttu-id="7ca58-129">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7ca58-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7ca58-130">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7ca58-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7ca58-131">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="7ca58-131">INPUTS</span></span>

### <span data-ttu-id="7ca58-132">System. String</span><span class="sxs-lookup"><span data-stu-id="7ca58-132">System.String</span></span>

## <span data-ttu-id="7ca58-133">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="7ca58-133">OUTPUTS</span></span>

### <span data-ttu-id="7ca58-134">Microsoft. Azure. Commands. SQL. Backup. model. AzureSqlDatabaseGeoBackupPolicyModel</span><span class="sxs-lookup"><span data-stu-id="7ca58-134">Microsoft.Azure.Commands.Sql.Backup.Model.AzureSqlDatabaseGeoBackupPolicyModel</span></span>

## <span data-ttu-id="7ca58-135">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="7ca58-135">NOTES</span></span>

## <span data-ttu-id="7ca58-136">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="7ca58-136">RELATED LINKS</span></span>

[<span data-ttu-id="7ca58-137">Get-AzureRmSqlDatabaseGeoBackupPolicy</span><span class="sxs-lookup"><span data-stu-id="7ca58-137">Get-AzureRmSqlDatabaseGeoBackupPolicy</span></span>](./Get-AzureRmSqlDatabaseGeoBackupPolicy.md)

[<span data-ttu-id="7ca58-138">Dokumentacja bazy danych SQL</span><span class="sxs-lookup"><span data-stu-id="7ca58-138">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)

