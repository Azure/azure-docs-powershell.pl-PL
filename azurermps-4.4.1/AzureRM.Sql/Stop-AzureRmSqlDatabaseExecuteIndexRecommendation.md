---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 4D2E0956-FBFA-43CC-ABE3-A6CBB9409263
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Stop-AzureRmSqlDatabaseExecuteIndexRecommendation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Stop-AzureRmSqlDatabaseExecuteIndexRecommendation.md
ms.openlocfilehash: 4fef918efd69d1ef5506efb70f1db94903845a8b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93718678"
---
# <span data-ttu-id="df097-101">Stop-AzureRmSqlDatabaseExecuteIndexRecommendation</span><span class="sxs-lookup"><span data-stu-id="df097-101">Stop-AzureRmSqlDatabaseExecuteIndexRecommendation</span></span>

## <span data-ttu-id="df097-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="df097-102">SYNOPSIS</span></span>
<span data-ttu-id="df097-103">Zatrzymuje przepływ pracy, w którym jest uruchamiana zalecana operacja indeksowania.</span><span class="sxs-lookup"><span data-stu-id="df097-103">Stops the workflow that runs a recommended index operation.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="df097-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="df097-104">SYNTAX</span></span>

```
Stop-AzureRmSqlDatabaseExecuteIndexRecommendation -ServerName <String> -DatabaseName <String>
 -IndexRecommendationName <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="df097-105">Opis</span><span class="sxs-lookup"><span data-stu-id="df097-105">DESCRIPTION</span></span>
<span data-ttu-id="df097-106">Polecenie cmdlet **stop-AzureRmSqlDatabaseExecuteIndexRecommendation** zatrzymuje przepływ pracy, w którym jest uruchamiana zalecana operacja indeksowania.</span><span class="sxs-lookup"><span data-stu-id="df097-106">The **Stop-AzureRmSqlDatabaseExecuteIndexRecommendation** cmdlet stops the workflow that runs a recommended index operation.</span></span>

## <span data-ttu-id="df097-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="df097-107">EXAMPLES</span></span>

### <span data-ttu-id="df097-108">Przykład 1: zatrzymywanie działania indeksu zalecenie</span><span class="sxs-lookup"><span data-stu-id="df097-108">Example 1: Stop running an index recommendation</span></span>
```
PS C:\>Stop-AzureRmSqlDatabaseExecuteIndexRecommendation -ResourceGroup "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -IndexRecommendationName "INDEX_NAME"
```

<span data-ttu-id="df097-109">To polecenie przestanie działać zalecenie dotyczące indeksu.</span><span class="sxs-lookup"><span data-stu-id="df097-109">This command stops running an index recommendation.</span></span>

## <span data-ttu-id="df097-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="df097-110">PARAMETERS</span></span>

### <span data-ttu-id="df097-111">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="df097-111">-DatabaseName</span></span>
<span data-ttu-id="df097-112">Określa nazwę bazy danych, dla której to polecenie cmdlet ma zatrzymywany przepływ pracy.</span><span class="sxs-lookup"><span data-stu-id="df097-112">Specifies the name of the database for which this cmdlet stops the workflow.</span></span>

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

### <span data-ttu-id="df097-113">-IndexRecommendationName</span><span class="sxs-lookup"><span data-stu-id="df097-113">-IndexRecommendationName</span></span>
<span data-ttu-id="df097-114">Określa nazwę zalecenia dotyczącego indeksu, które zostanie zatrzymane przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="df097-114">Specifies the name of the index recommendation that this cmdlet stops.</span></span>

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

### <span data-ttu-id="df097-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="df097-115">-ResourceGroupName</span></span>
<span data-ttu-id="df097-116">Określa nazwę grupy zasobów, do której jest przypisany serwer.</span><span class="sxs-lookup"><span data-stu-id="df097-116">Specifies the name of the resource group to which the server is assigned.</span></span>

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

### <span data-ttu-id="df097-117">-Nazwa_serwera</span><span class="sxs-lookup"><span data-stu-id="df097-117">-ServerName</span></span>
<span data-ttu-id="df097-118">Określa serwer hostujący bazę danych, dla której to polecenie cmdlet ma zatrzymywany przepływ pracy.</span><span class="sxs-lookup"><span data-stu-id="df097-118">Specifies the server that hosts the database for which this cmdlet stops a workflow.</span></span>

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

### <span data-ttu-id="df097-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="df097-119">-DefaultProfile</span></span>
<span data-ttu-id="df097-120">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="df097-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="df097-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="df097-121">CommonParameters</span></span>
<span data-ttu-id="df097-122">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="df097-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="df097-123">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="df097-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="df097-124">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="df097-124">INPUTS</span></span>

## <span data-ttu-id="df097-125">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="df097-125">OUTPUTS</span></span>

## <span data-ttu-id="df097-126">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="df097-126">NOTES</span></span>

## <span data-ttu-id="df097-127">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="df097-127">RELATED LINKS</span></span>

[<span data-ttu-id="df097-128">Get-AzureRmSqlDatabaseIndexRecommendations</span><span class="sxs-lookup"><span data-stu-id="df097-128">Get-AzureRmSqlDatabaseIndexRecommendations</span></span>](./Get-AzureRmSqlDatabaseIndexRecommendations.md)

[<span data-ttu-id="df097-129">Start — AzureRmSqlDatabaseExecuteIndexRecommendation</span><span class="sxs-lookup"><span data-stu-id="df097-129">Start-AzureRmSqlDatabaseExecuteIndexRecommendation</span></span>](./Start-AzureRmSqlDatabaseExecuteIndexRecommendation.md)

[<span data-ttu-id="df097-130">Dokumentacja bazy danych SQL</span><span class="sxs-lookup"><span data-stu-id="df097-130">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


