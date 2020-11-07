---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 40054224-52FF-4AF6-A090-9F6D07A2BA99
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqldatabasereplicationlink
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseReplicationLink.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseReplicationLink.md
ms.openlocfilehash: 6bb2a3891abe8453ee8460f6879dbc134f6ab29b
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93707984"
---
# <span data-ttu-id="ce838-101">Get-AzSqlDatabaseReplicationLink</span><span class="sxs-lookup"><span data-stu-id="ce838-101">Get-AzSqlDatabaseReplicationLink</span></span>

## <span data-ttu-id="ce838-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="ce838-102">SYNOPSIS</span></span>
<span data-ttu-id="ce838-103">Pobiera linki replikacji geograficznej między bazą danych SQL Azure a grupą zasobów lub programem SQL Server.</span><span class="sxs-lookup"><span data-stu-id="ce838-103">Gets the geo-replication links between an Azure SQL Database and a resource group or SQL Server.</span></span>

## <span data-ttu-id="ce838-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="ce838-104">SYNTAX</span></span>

```
Get-AzSqlDatabaseReplicationLink [-DatabaseName] <String> -PartnerResourceGroupName <String>
 [-PartnerServerName <String>] [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ce838-105">Opis</span><span class="sxs-lookup"><span data-stu-id="ce838-105">DESCRIPTION</span></span>
<span data-ttu-id="ce838-106">Polecenie cmdlet **Get-AzSqlDatabaseReplicationLink** zastępuje polecenie cmdlet **Get-AzSqlDatabaseCopy** .</span><span class="sxs-lookup"><span data-stu-id="ce838-106">The **Get-AzSqlDatabaseReplicationLink** cmdlet replaces the **Get-AzSqlDatabaseCopy** cmdlet.</span></span>
<span data-ttu-id="ce838-107">Wszystkie linki replikacji geograficznej między określoną bazą danych SQL Azure a grupą zasobów lub serwerem AzureSQL.</span><span class="sxs-lookup"><span data-stu-id="ce838-107">It gets all geo-replication links between the specified Azure SQL Database and a resource group or AzureSQL Server.</span></span>

## <span data-ttu-id="ce838-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="ce838-108">EXAMPLES</span></span>

## <span data-ttu-id="ce838-109">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="ce838-109">PARAMETERS</span></span>

### <span data-ttu-id="ce838-110">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="ce838-110">-DatabaseName</span></span>
<span data-ttu-id="ce838-111">Określa nazwę bazy danych SQL, dla której mają zostać pobrane linki.</span><span class="sxs-lookup"><span data-stu-id="ce838-111">Specifies the name of the SQL Database for which to retrieve links.</span></span>

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

### <span data-ttu-id="ce838-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ce838-112">-DefaultProfile</span></span>
<span data-ttu-id="ce838-113">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="ce838-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ce838-114">-PartnerResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ce838-114">-PartnerResourceGroupName</span></span>
<span data-ttu-id="ce838-115">Określa nazwę grupy zasobów, do której jest przypisany dany partner.</span><span class="sxs-lookup"><span data-stu-id="ce838-115">Specifies the name of the resource group to which the partner is assigned.</span></span>

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

### <span data-ttu-id="ce838-116">-PartnerServerName</span><span class="sxs-lookup"><span data-stu-id="ce838-116">-PartnerServerName</span></span>
<span data-ttu-id="ce838-117">Określa nazwę usługi Azure SQL Server dla partnera.</span><span class="sxs-lookup"><span data-stu-id="ce838-117">Specifies the name of the Azure SQL Server for the partner.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: True
```

### <span data-ttu-id="ce838-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ce838-118">-ResourceGroupName</span></span>
<span data-ttu-id="ce838-119">Określa nazwę grupy zasobów platformy Azure dla bazy danych, dla której mają zostać pobrane linki.</span><span class="sxs-lookup"><span data-stu-id="ce838-119">Specifies the name of the Azure resource group for the database for which to retrieve links.</span></span>

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

### <span data-ttu-id="ce838-120">-Nazwa_serwera</span><span class="sxs-lookup"><span data-stu-id="ce838-120">-ServerName</span></span>
<span data-ttu-id="ce838-121">Określa nazwę serwera SQL, dla którego baza danych ma pobierać linki.</span><span class="sxs-lookup"><span data-stu-id="ce838-121">Specifies the name of the SQL Server for the database to retrieve links for.</span></span>

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

### <span data-ttu-id="ce838-122">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="ce838-122">-Confirm</span></span>
<span data-ttu-id="ce838-123">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ce838-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ce838-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ce838-124">-WhatIf</span></span>
<span data-ttu-id="ce838-125">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ce838-125">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="ce838-126">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="ce838-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ce838-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ce838-127">CommonParameters</span></span>
<span data-ttu-id="ce838-128">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ce838-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ce838-129">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ce838-129">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ce838-130">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ce838-130">INPUTS</span></span>

### <span data-ttu-id="ce838-131">System. String</span><span class="sxs-lookup"><span data-stu-id="ce838-131">System.String</span></span>

## <span data-ttu-id="ce838-132">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="ce838-132">OUTPUTS</span></span>

### <span data-ttu-id="ce838-133">Microsoft. Azure. Commands. SQL. Replication. model. AzureReplicationLinkModel</span><span class="sxs-lookup"><span data-stu-id="ce838-133">Microsoft.Azure.Commands.Sql.Replication.Model.AzureReplicationLinkModel</span></span>

## <span data-ttu-id="ce838-134">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="ce838-134">NOTES</span></span>

## <span data-ttu-id="ce838-135">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="ce838-135">RELATED LINKS</span></span>

[<span data-ttu-id="ce838-136">Dokumentacja bazy danych SQL</span><span class="sxs-lookup"><span data-stu-id="ce838-136">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)