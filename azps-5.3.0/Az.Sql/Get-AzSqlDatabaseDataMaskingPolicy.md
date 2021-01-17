---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: FFC02A5D-A12F-494D-8542-76A5B89E32DC
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqldatabasedatamaskingpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseDataMaskingPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseDataMaskingPolicy.md
ms.openlocfilehash: 8fb1b8125a6fd0c42bedc00733f3a128846673e4
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98375081"
---
# <span data-ttu-id="0de42-101">Get-AzSqlDatabaseDataMaskingPolicy</span><span class="sxs-lookup"><span data-stu-id="0de42-101">Get-AzSqlDatabaseDataMaskingPolicy</span></span>

## <span data-ttu-id="0de42-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="0de42-102">SYNOPSIS</span></span>
<span data-ttu-id="0de42-103">Pobiera zasady maskowania danych dla bazy danych.</span><span class="sxs-lookup"><span data-stu-id="0de42-103">Gets the data masking policy for a database.</span></span>

## <span data-ttu-id="0de42-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="0de42-104">SYNTAX</span></span>

```
Get-AzSqlDatabaseDataMaskingPolicy [-ServerName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="0de42-105">Opis</span><span class="sxs-lookup"><span data-stu-id="0de42-105">DESCRIPTION</span></span>
<span data-ttu-id="0de42-106">Polecenie cmdlet **Get-AzSqlDatabaseDataMaskingPolicy** pobiera zasady maskowania danych bazy danych Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="0de42-106">The **Get-AzSqlDatabaseDataMaskingPolicy** cmdlet gets the data masking policy of an Azure SQL database.</span></span>
<span data-ttu-id="0de42-107">Aby użyć tego polecenia cmdlet, użyj parametrów *ResourceGroupName*, *nazwa_serwera* i *DatabaseName* w celu zidentyfikowania bazy danych.</span><span class="sxs-lookup"><span data-stu-id="0de42-107">To use this cmdlet, use the *ResourceGroupName*, *ServerName*, and *DatabaseName* parameters to identify the database.</span></span>
<span data-ttu-id="0de42-108">To polecenie cmdlet jest również obsługiwane przez usługę bazy danych SQL Server undatabase na platformie Azure.</span><span class="sxs-lookup"><span data-stu-id="0de42-108">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

## <span data-ttu-id="0de42-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="0de42-109">EXAMPLES</span></span>

### <span data-ttu-id="0de42-110">Przykład 1: pobieranie zasad maskowania danych dla bazy danych Azure SQL Database</span><span class="sxs-lookup"><span data-stu-id="0de42-110">Example 1: Get the data masking policy for an Azure SQL database</span></span>
```
PS C:\>Get-AzSqlDatabaseDataMaskingPolicy -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
DatabaseName      : Database01
ResourceGroupName : ResourceGroup01
ServerName        : Server01
DataMaskingState  : Enabled
PrivilegedUsers  :
```

<span data-ttu-id="0de42-111">To polecenie uzyskuje zasady maskowania danych z bazy danych Database01 w grupie zasób ResourceGroup01 na serwerze Server01.</span><span class="sxs-lookup"><span data-stu-id="0de42-111">This command gets the data masking policy from database Database01 in resource group ResourceGroup01 on server Server01.</span></span>

## <span data-ttu-id="0de42-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="0de42-112">PARAMETERS</span></span>

### <span data-ttu-id="0de42-113">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="0de42-113">-DatabaseName</span></span>
<span data-ttu-id="0de42-114">Określa nazwę bazy danych.</span><span class="sxs-lookup"><span data-stu-id="0de42-114">Specifies the name of the database.</span></span>

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

### <span data-ttu-id="0de42-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0de42-115">-DefaultProfile</span></span>
<span data-ttu-id="0de42-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="0de42-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="0de42-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0de42-117">-ResourceGroupName</span></span>
<span data-ttu-id="0de42-118">Określa nazwę grupy zasobów, do której jest przypisana baza danych.</span><span class="sxs-lookup"><span data-stu-id="0de42-118">Specifies the name of the resource group to which the database is assigned.</span></span>

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

### <span data-ttu-id="0de42-119">-Nazwa_serwera</span><span class="sxs-lookup"><span data-stu-id="0de42-119">-ServerName</span></span>
<span data-ttu-id="0de42-120">Określa nazwę serwera, na którym znajduje się baza danych.</span><span class="sxs-lookup"><span data-stu-id="0de42-120">Specifies the name of the server where the database is located.</span></span>

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

### <span data-ttu-id="0de42-121">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="0de42-121">-Confirm</span></span>
<span data-ttu-id="0de42-122">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0de42-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0de42-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0de42-123">-WhatIf</span></span>
<span data-ttu-id="0de42-124">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0de42-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0de42-125">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="0de42-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0de42-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0de42-126">CommonParameters</span></span>
<span data-ttu-id="0de42-127">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0de42-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0de42-128">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="0de42-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0de42-129">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="0de42-129">INPUTS</span></span>

### <span data-ttu-id="0de42-130">System. String</span><span class="sxs-lookup"><span data-stu-id="0de42-130">System.String</span></span>

## <span data-ttu-id="0de42-131">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="0de42-131">OUTPUTS</span></span>

### <span data-ttu-id="0de42-132">Microsoft. Azure. Commands. SQL. datamaskowania. model. DatabaseDataMaskingPolicyModel</span><span class="sxs-lookup"><span data-stu-id="0de42-132">Microsoft.Azure.Commands.Sql.DataMasking.Model.DatabaseDataMaskingPolicyModel</span></span>

## <span data-ttu-id="0de42-133">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="0de42-133">NOTES</span></span>

## <span data-ttu-id="0de42-134">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="0de42-134">RELATED LINKS</span></span>

[<span data-ttu-id="0de42-135">Get-AzSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="0de42-135">Get-AzSqlDatabaseDataMaskingRule</span></span>](./Get-AzSqlDatabaseDataMaskingRule.md)

[<span data-ttu-id="0de42-136">Nowe — AzSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="0de42-136">New-AzSqlDatabaseDataMaskingRule</span></span>](./New-AzSqlDatabaseDataMaskingRule.md)

[<span data-ttu-id="0de42-137">Remove-AzSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="0de42-137">Remove-AzSqlDatabaseDataMaskingRule</span></span>](./Remove-AzSqlDatabaseDataMaskingRule.md)

[<span data-ttu-id="0de42-138">Set-AzSqlDatabaseDataMaskingPolicy</span><span class="sxs-lookup"><span data-stu-id="0de42-138">Set-AzSqlDatabaseDataMaskingPolicy</span></span>](./Set-AzSqlDatabaseDataMaskingPolicy.md)

[<span data-ttu-id="0de42-139">Set-AzSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="0de42-139">Set-AzSqlDatabaseDataMaskingRule</span></span>](./Set-AzSqlDatabaseDataMaskingRule.md)


