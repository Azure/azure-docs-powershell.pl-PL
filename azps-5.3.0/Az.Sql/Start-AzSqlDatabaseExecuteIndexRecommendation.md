---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 0EA0B131-A3D0-43CA-8517-9E724A11B04F
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/start-azsqldatabaseexecuteindexrecommendation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Start-AzSqlDatabaseExecuteIndexRecommendation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Start-AzSqlDatabaseExecuteIndexRecommendation.md
ms.openlocfilehash: e69cffe6955a5bf19636dd519c0906be64ce4413
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98499762"
---
# <span data-ttu-id="71c17-101">Start-AzSqlDatabaseExecuteIndexRecommendation</span><span class="sxs-lookup"><span data-stu-id="71c17-101">Start-AzSqlDatabaseExecuteIndexRecommendation</span></span>

## <span data-ttu-id="71c17-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="71c17-102">SYNOPSIS</span></span>
<span data-ttu-id="71c17-103">Uruchamia przepływ pracy, w którym jest uruchamiana zalecana operacja indeksowania.</span><span class="sxs-lookup"><span data-stu-id="71c17-103">Starts the workflow that runs a recommended index operation.</span></span>

## <span data-ttu-id="71c17-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="71c17-104">SYNTAX</span></span>

```
Start-AzSqlDatabaseExecuteIndexRecommendation -ServerName <String> -DatabaseName <String>
 -IndexRecommendationName <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="71c17-105">Opis</span><span class="sxs-lookup"><span data-stu-id="71c17-105">DESCRIPTION</span></span>
<span data-ttu-id="71c17-106">Polecenie cmdlet **Start-AzSqlDatabaseExecuteIndexRecommendation** uruchamia przepływ pracy, w którym jest uruchamiana zalecana operacja indeksowania dla bazy danych SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="71c17-106">The **Start-AzSqlDatabaseExecuteIndexRecommendation** cmdlet starts the workflow that runs a recommended index operation for an Azure SQL Database.</span></span>

## <span data-ttu-id="71c17-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="71c17-107">EXAMPLES</span></span>

### <span data-ttu-id="71c17-108">Przykład 1. Uruchom zalecenie dotyczące indeksu</span><span class="sxs-lookup"><span data-stu-id="71c17-108">Example 1: Run an index recommendation</span></span>
```
PS C:\>Start-AzSqlDatabaseExecuteIndexRecommendation -ResourceGroup "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -IndexRecommendationName "INDEX_NAME"
```

<span data-ttu-id="71c17-109">To polecenie uruchamia zalecenie indeksu.</span><span class="sxs-lookup"><span data-stu-id="71c17-109">This command runs an index recommendation.</span></span>

## <span data-ttu-id="71c17-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="71c17-110">PARAMETERS</span></span>

### <span data-ttu-id="71c17-111">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="71c17-111">-DatabaseName</span></span>
<span data-ttu-id="71c17-112">Określa nazwę bazy danych, dla której to polecenie cmdlet uruchamia przepływ pracy.</span><span class="sxs-lookup"><span data-stu-id="71c17-112">Specifies the name of the database for which this cmdlet starts the workflow.</span></span>

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

### <span data-ttu-id="71c17-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="71c17-113">-DefaultProfile</span></span>
<span data-ttu-id="71c17-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="71c17-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="71c17-115">-IndexRecommendationName</span><span class="sxs-lookup"><span data-stu-id="71c17-115">-IndexRecommendationName</span></span>
<span data-ttu-id="71c17-116">Określa nazwę zalecenia dotyczącego indeksu, które zostanie uruchomione przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="71c17-116">Specifies the name of the index recommendation that this cmdlet runs.</span></span>

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

### <span data-ttu-id="71c17-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="71c17-117">-ResourceGroupName</span></span>
<span data-ttu-id="71c17-118">Określa nazwę grupy zasobów, do której jest przypisany serwer.</span><span class="sxs-lookup"><span data-stu-id="71c17-118">Specifies the name of the resource group to which the server is assigned.</span></span>

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

### <span data-ttu-id="71c17-119">-Nazwa_serwera</span><span class="sxs-lookup"><span data-stu-id="71c17-119">-ServerName</span></span>
<span data-ttu-id="71c17-120">Określa serwer, na którym znajduje się baza danych, dla której ten polecenie cmdlet rozpoczyna przepływ pracy.</span><span class="sxs-lookup"><span data-stu-id="71c17-120">Specifies the server that hosts the database for which this cmdlet starts a workflow.</span></span>

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

### <span data-ttu-id="71c17-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="71c17-121">CommonParameters</span></span>
<span data-ttu-id="71c17-122">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="71c17-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="71c17-123">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="71c17-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="71c17-124">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="71c17-124">INPUTS</span></span>

### <span data-ttu-id="71c17-125">System. String</span><span class="sxs-lookup"><span data-stu-id="71c17-125">System.String</span></span>

## <span data-ttu-id="71c17-126">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="71c17-126">OUTPUTS</span></span>

### <span data-ttu-id="71c17-127">Microsoft. Azure. Commands. SQL. model. IndexRecommendation</span><span class="sxs-lookup"><span data-stu-id="71c17-127">Microsoft.Azure.Commands.Sql.Model.IndexRecommendation</span></span>

## <span data-ttu-id="71c17-128">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="71c17-128">NOTES</span></span>

## <span data-ttu-id="71c17-129">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="71c17-129">RELATED LINKS</span></span>

[<span data-ttu-id="71c17-130">Get-AzSqlDatabaseIndexRecommendation</span><span class="sxs-lookup"><span data-stu-id="71c17-130">Get-AzSqlDatabaseIndexRecommendation</span></span>](./Get-AzSqlDatabaseIndexRecommendation.md)

[<span data-ttu-id="71c17-131">Zatrzymaj — AzSqlDatabaseExecuteIndexRecommendation</span><span class="sxs-lookup"><span data-stu-id="71c17-131">Stop-AzSqlDatabaseExecuteIndexRecommendation</span></span>](./Stop-AzSqlDatabaseExecuteIndexRecommendation.md)

[<span data-ttu-id="71c17-132">Dokumentacja bazy danych SQL</span><span class="sxs-lookup"><span data-stu-id="71c17-132">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


