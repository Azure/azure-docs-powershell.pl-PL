---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 0EA0B131-A3D0-43CA-8517-9E724A11B04F
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/start-azsqldatabaseexecuteindexrecommendation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Start-AzSqlDatabaseExecuteIndexRecommendation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Start-AzSqlDatabaseExecuteIndexRecommendation.md
ms.openlocfilehash: c432b3a23c4495abebda013b5dd3943132827a30
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93887713"
---
# <span data-ttu-id="5a59f-101">Start-AzSqlDatabaseExecuteIndexRecommendation</span><span class="sxs-lookup"><span data-stu-id="5a59f-101">Start-AzSqlDatabaseExecuteIndexRecommendation</span></span>

## <span data-ttu-id="5a59f-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="5a59f-102">SYNOPSIS</span></span>
<span data-ttu-id="5a59f-103">Uruchamia przepływ pracy, w którym jest uruchamiana zalecana operacja indeksowania.</span><span class="sxs-lookup"><span data-stu-id="5a59f-103">Starts the workflow that runs a recommended index operation.</span></span>

## <span data-ttu-id="5a59f-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="5a59f-104">SYNTAX</span></span>

```
Start-AzSqlDatabaseExecuteIndexRecommendation -ServerName <String> -DatabaseName <String>
 -IndexRecommendationName <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="5a59f-105">Opis</span><span class="sxs-lookup"><span data-stu-id="5a59f-105">DESCRIPTION</span></span>
<span data-ttu-id="5a59f-106">Polecenie cmdlet **Start-AzSqlDatabaseExecuteIndexRecommendation** uruchamia przepływ pracy, w którym jest uruchamiana zalecana operacja indeksowania dla bazy danych SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="5a59f-106">The **Start-AzSqlDatabaseExecuteIndexRecommendation** cmdlet starts the workflow that runs a recommended index operation for an Azure SQL Database.</span></span>

## <span data-ttu-id="5a59f-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="5a59f-107">EXAMPLES</span></span>

### <span data-ttu-id="5a59f-108">Przykład 1. Uruchom zalecenie dotyczące indeksu</span><span class="sxs-lookup"><span data-stu-id="5a59f-108">Example 1: Run an index recommendation</span></span>
```
PS C:\>Start-AzSqlDatabaseExecuteIndexRecommendation -ResourceGroup "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -IndexRecommendationName "INDEX_NAME"
```

<span data-ttu-id="5a59f-109">To polecenie uruchamia zalecenie indeksu.</span><span class="sxs-lookup"><span data-stu-id="5a59f-109">This command runs an index recommendation.</span></span>

## <span data-ttu-id="5a59f-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="5a59f-110">PARAMETERS</span></span>

### <span data-ttu-id="5a59f-111">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="5a59f-111">-DatabaseName</span></span>
<span data-ttu-id="5a59f-112">Określa nazwę bazy danych, dla której to polecenie cmdlet uruchamia przepływ pracy.</span><span class="sxs-lookup"><span data-stu-id="5a59f-112">Specifies the name of the database for which this cmdlet starts the workflow.</span></span>

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

### <span data-ttu-id="5a59f-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5a59f-113">-DefaultProfile</span></span>
<span data-ttu-id="5a59f-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="5a59f-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="5a59f-115">-IndexRecommendationName</span><span class="sxs-lookup"><span data-stu-id="5a59f-115">-IndexRecommendationName</span></span>
<span data-ttu-id="5a59f-116">Określa nazwę zalecenia dotyczącego indeksu, które zostanie uruchomione przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5a59f-116">Specifies the name of the index recommendation that this cmdlet runs.</span></span>

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

### <span data-ttu-id="5a59f-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5a59f-117">-ResourceGroupName</span></span>
<span data-ttu-id="5a59f-118">Określa nazwę grupy zasobów, do której jest przypisany serwer.</span><span class="sxs-lookup"><span data-stu-id="5a59f-118">Specifies the name of the resource group to which the server is assigned.</span></span>

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

### <span data-ttu-id="5a59f-119">-Nazwa_serwera</span><span class="sxs-lookup"><span data-stu-id="5a59f-119">-ServerName</span></span>
<span data-ttu-id="5a59f-120">Określa serwer, na którym znajduje się baza danych, dla której ten polecenie cmdlet rozpoczyna przepływ pracy.</span><span class="sxs-lookup"><span data-stu-id="5a59f-120">Specifies the server that hosts the database for which this cmdlet starts a workflow.</span></span>

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

### <span data-ttu-id="5a59f-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5a59f-121">CommonParameters</span></span>
<span data-ttu-id="5a59f-122">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5a59f-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5a59f-123">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="5a59f-123">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5a59f-124">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="5a59f-124">INPUTS</span></span>

### <span data-ttu-id="5a59f-125">System. String</span><span class="sxs-lookup"><span data-stu-id="5a59f-125">System.String</span></span>

## <span data-ttu-id="5a59f-126">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="5a59f-126">OUTPUTS</span></span>

### <span data-ttu-id="5a59f-127">Microsoft. Azure. Commands. SQL. model. IndexRecommendation</span><span class="sxs-lookup"><span data-stu-id="5a59f-127">Microsoft.Azure.Commands.Sql.Model.IndexRecommendation</span></span>

## <span data-ttu-id="5a59f-128">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="5a59f-128">NOTES</span></span>

## <span data-ttu-id="5a59f-129">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="5a59f-129">RELATED LINKS</span></span>

[<span data-ttu-id="5a59f-130">Get-AzSqlDatabaseIndexRecommendations</span><span class="sxs-lookup"><span data-stu-id="5a59f-130">Get-AzSqlDatabaseIndexRecommendations</span></span>](./Get-AzSqlDatabaseIndexRecommendations.md)

[<span data-ttu-id="5a59f-131">Zatrzymaj — AzSqlDatabaseExecuteIndexRecommendation</span><span class="sxs-lookup"><span data-stu-id="5a59f-131">Stop-AzSqlDatabaseExecuteIndexRecommendation</span></span>](./Stop-AzSqlDatabaseExecuteIndexRecommendation.md)

[<span data-ttu-id="5a59f-132">Dokumentacja bazy danych SQL</span><span class="sxs-lookup"><span data-stu-id="5a59f-132">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


