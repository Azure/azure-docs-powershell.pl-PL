---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 40054224-52FF-4AF6-A090-9F6D07A2BA99
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/get-azurermsqldatabasereplicationlink
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlDatabaseReplicationLink.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlDatabaseReplicationLink.md
ms.openlocfilehash: 993d7ef8958e96cebcd104d25550e860cdfd1853
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93550211"
---
# <span data-ttu-id="d933b-101">Get-AzureRmSqlDatabaseReplicationLink</span><span class="sxs-lookup"><span data-stu-id="d933b-101">Get-AzureRmSqlDatabaseReplicationLink</span></span>

## <span data-ttu-id="d933b-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="d933b-102">SYNOPSIS</span></span>
<span data-ttu-id="d933b-103">Pobiera linki replikacji geograficznej między bazą danych SQL Azure a grupą zasobów lub programem SQL Server.</span><span class="sxs-lookup"><span data-stu-id="d933b-103">Gets the geo-replication links between an Azure SQL Database and a resource group or SQL Server.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d933b-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="d933b-104">SYNTAX</span></span>

### <span data-ttu-id="d933b-105">ByDatabaseName (domyślny)</span><span class="sxs-lookup"><span data-stu-id="d933b-105">ByDatabaseName (Default)</span></span>
```
Get-AzureRmSqlDatabaseReplicationLink [-DatabaseName] <String> -PartnerResourceGroupName <String>
 [-ServerName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d933b-106">ByPartnerServerName</span><span class="sxs-lookup"><span data-stu-id="d933b-106">ByPartnerServerName</span></span>
```
Get-AzureRmSqlDatabaseReplicationLink [-DatabaseName] <String> -PartnerResourceGroupName <String>
 [-PartnerServerName <String>] [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d933b-107">Opis</span><span class="sxs-lookup"><span data-stu-id="d933b-107">DESCRIPTION</span></span>
<span data-ttu-id="d933b-108">Polecenie cmdlet **Get-AzureRMSqlDatabaseReplicationLink** zastępuje polecenie cmdlet **Get-AzureSqlDatabaseCopy** .</span><span class="sxs-lookup"><span data-stu-id="d933b-108">The **Get-AzureRMSqlDatabaseReplicationLink** cmdlet replaces the **Get-AzureSqlDatabaseCopy** cmdlet.</span></span>
<span data-ttu-id="d933b-109">Wszystkie linki replikacji geograficznej między określoną bazą danych SQL Azure a grupą zasobów lub serwerem AzureSQL.</span><span class="sxs-lookup"><span data-stu-id="d933b-109">It gets all geo-replication links between the specified Azure SQL Database and a resource group or AzureSQL Server.</span></span>

## <span data-ttu-id="d933b-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="d933b-110">EXAMPLES</span></span>

## <span data-ttu-id="d933b-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="d933b-111">PARAMETERS</span></span>

### <span data-ttu-id="d933b-112">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="d933b-112">-DatabaseName</span></span>
<span data-ttu-id="d933b-113">Określa nazwę bazy danych SQL, dla której mają zostać pobrane linki.</span><span class="sxs-lookup"><span data-stu-id="d933b-113">Specifies the name of the SQL Database for which to retrieve links.</span></span>

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

### <span data-ttu-id="d933b-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d933b-114">-DefaultProfile</span></span>
<span data-ttu-id="d933b-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="d933b-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d933b-116">-PartnerResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d933b-116">-PartnerResourceGroupName</span></span>
<span data-ttu-id="d933b-117">Określa nazwę grupy zasobów, do której jest przypisany dany partner.</span><span class="sxs-lookup"><span data-stu-id="d933b-117">Specifies the name of the resource group to which the partner is assigned.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d933b-118">-PartnerServerName</span><span class="sxs-lookup"><span data-stu-id="d933b-118">-PartnerServerName</span></span>
<span data-ttu-id="d933b-119">Określa nazwę usługi Azure SQL Server dla partnera.</span><span class="sxs-lookup"><span data-stu-id="d933b-119">Specifies the name of the Azure SQL Server for the partner.</span></span>

```yaml
Type: System.String
Parameter Sets: ByPartnerServerName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d933b-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d933b-120">-ResourceGroupName</span></span>
<span data-ttu-id="d933b-121">Określa nazwę grupy zasobów platformy Azure dla bazy danych, dla której mają zostać pobrane linki.</span><span class="sxs-lookup"><span data-stu-id="d933b-121">Specifies the name of the Azure resource group for the database for which to retrieve links.</span></span>

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

### <span data-ttu-id="d933b-122">-Nazwa_serwera</span><span class="sxs-lookup"><span data-stu-id="d933b-122">-ServerName</span></span>
<span data-ttu-id="d933b-123">Określa nazwę serwera SQL, dla którego baza danych ma pobierać linki.</span><span class="sxs-lookup"><span data-stu-id="d933b-123">Specifies the name of the SQL Server for the database to retrieve links for.</span></span>

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

### <span data-ttu-id="d933b-124">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="d933b-124">-Confirm</span></span>
<span data-ttu-id="d933b-125">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d933b-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d933b-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d933b-126">-WhatIf</span></span>
<span data-ttu-id="d933b-127">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d933b-127">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="d933b-128">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="d933b-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d933b-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d933b-129">CommonParameters</span></span>
<span data-ttu-id="d933b-130">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d933b-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d933b-131">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d933b-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d933b-132">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d933b-132">INPUTS</span></span>

### <span data-ttu-id="d933b-133">System. String</span><span class="sxs-lookup"><span data-stu-id="d933b-133">System.String</span></span>

## <span data-ttu-id="d933b-134">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="d933b-134">OUTPUTS</span></span>

### <span data-ttu-id="d933b-135">Microsoft. Azure. Commands. SQL. Replication. model. AzureReplicationLinkModel</span><span class="sxs-lookup"><span data-stu-id="d933b-135">Microsoft.Azure.Commands.Sql.Replication.Model.AzureReplicationLinkModel</span></span>

## <span data-ttu-id="d933b-136">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="d933b-136">NOTES</span></span>

## <span data-ttu-id="d933b-137">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="d933b-137">RELATED LINKS</span></span>

[<span data-ttu-id="d933b-138">Dokumentacja bazy danych SQL</span><span class="sxs-lookup"><span data-stu-id="d933b-138">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
