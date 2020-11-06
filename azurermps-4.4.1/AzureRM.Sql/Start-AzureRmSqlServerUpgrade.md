---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 69A26BF3-7FE7-41ED-8C21-C8DC72D09615
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Start-AzureRmSqlServerUpgrade.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Start-AzureRmSqlServerUpgrade.md
ms.openlocfilehash: bd61b666dd321ec9007d413030cb899eeeb92778
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93552319"
---
# <span data-ttu-id="fc1bc-101">Start-AzureRmSqlServerUpgrade</span><span class="sxs-lookup"><span data-stu-id="fc1bc-101">Start-AzureRmSqlServerUpgrade</span></span>

## <span data-ttu-id="fc1bc-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="fc1bc-102">SYNOPSIS</span></span>
<span data-ttu-id="fc1bc-103">Rozpoczynanie uaktualniania serwera bazy danych SQL.</span><span class="sxs-lookup"><span data-stu-id="fc1bc-103">Starts the upgrade of a SQL Database server.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fc1bc-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="fc1bc-104">SYNTAX</span></span>

```
Start-AzureRmSqlServerUpgrade -ServerVersion <String> [-ScheduleUpgradeAfterUtcDateTime <DateTime>]
 [-DatabaseCollection <RecommendedDatabaseProperties[]>]
 [-ElasticPoolCollection <UpgradeRecommendedElasticPoolProperties[]>] -ServerName <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fc1bc-105">Opis</span><span class="sxs-lookup"><span data-stu-id="fc1bc-105">DESCRIPTION</span></span>
<span data-ttu-id="fc1bc-106">Polecenie cmdlet **Start-AzureRmSqlServerUpgrade** rozpoczyna uaktualnianie serwera bazy danych SQL Azure w wersji 11 do wersji 12.</span><span class="sxs-lookup"><span data-stu-id="fc1bc-106">The **Start-AzureRmSqlServerUpgrade** cmdlet starts the upgrade of an Azure SQL Database server version 11 to version 12.</span></span>
<span data-ttu-id="fc1bc-107">Postęp uaktualnienia można monitorować przy użyciu Get-AzureRmSqlServerUpgrade polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fc1bc-107">You can monitor the progress of an upgrade by using the Get-AzureRmSqlServerUpgrade cmdlet.</span></span>

## <span data-ttu-id="fc1bc-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="fc1bc-108">EXAMPLES</span></span>

### <span data-ttu-id="fc1bc-109">Przykład 1: uaktualnianie serwera</span><span class="sxs-lookup"><span data-stu-id="fc1bc-109">Example 1: Upgrade a server</span></span>
```
PS C:\>Start-AzureRmSqlServerUpgrade -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -ServerVersion 12.0
ResourceGroupName               : ResourceGroup01
ServerName                      : Server01
ServerVersion                   : 12.0
ScheduleUpgradeAfterUtcDateTime : 
DatabaseCollection              :
```

<span data-ttu-id="fc1bc-110">To polecenie uaktualnia serwer o nazwie Server01 przypisany do TesourceGroup01 grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="fc1bc-110">This command upgrades the server named server01 assigned to resource group TesourceGroup01.</span></span>

### <span data-ttu-id="fc1bc-111">Przykład 2: uaktualnianie serwera za pomocą harmonogramu i zaleceń dotyczących bazy danych</span><span class="sxs-lookup"><span data-stu-id="fc1bc-111">Example 2: Upgrade a server by using schedule time and database recommendation</span></span>
```
PS C:\>$ScheduleTime = (Get-Date).AddMinutes(5).ToUniversalTime()
PS C:\> $DatabaseMap = New-Object -TypeName Microsoft.Azure.Management.Sql.Models.RecommendedDatabaseProperties
PS C:\> $DatabaseMap.Name = "contosodb"
PS C:\> $DatabaseMap.TargetEdition = "Standard"
PS C:\> $DatabaseMap.TargetServiceLevelObjective = "S0"
PS C:\> Start-AzureRmSqlServerUpgrade -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -ServerVersion 12.0 -ScheduleUpgradeAfterUtcDateTime $ScheduleTime -DatabaseCollection ($DatabaseMap)
```

<span data-ttu-id="fc1bc-112">Pierwsze polecenie w przyszłości tworzy godzinę w ciągu pięciu minut, korzystając z polecenia cmdlet Get-Date.</span><span class="sxs-lookup"><span data-stu-id="fc1bc-112">The first command creates a time five minutes in the future by using the Get-Date cmdlet.</span></span>
<span data-ttu-id="fc1bc-113">Polecenie zapisuje datę w zmiennej $ScheduleTime.</span><span class="sxs-lookup"><span data-stu-id="fc1bc-113">The command stores the date in the variable $ScheduleTime.</span></span>
<span data-ttu-id="fc1bc-114">Aby uzyskać więcej informacji, wpisz tekst `Get-Help Get-Date` .</span><span class="sxs-lookup"><span data-stu-id="fc1bc-114">For more information, type `Get-Help Get-Date`.</span></span>

<span data-ttu-id="fc1bc-115">Drugie polecenie tworzy obiekt **RecommendedDatabaseProperties** , a następnie zapisuje ten obiekt w zmiennej $DatabaseMap.</span><span class="sxs-lookup"><span data-stu-id="fc1bc-115">The second command creates a **RecommendedDatabaseProperties** object, and then stores that object in the variable $DatabaseMap.</span></span>

<span data-ttu-id="fc1bc-116">Kolejne trzy polecenia przypisują wartości do właściwości obiektu przechowywanego w $DatabaseMap.</span><span class="sxs-lookup"><span data-stu-id="fc1bc-116">The next three commands assign values to properties of the object stored in $DatabaseMap.</span></span>

<span data-ttu-id="fc1bc-117">Ostatnie polecenie uaktualnia istniejący serwer o nazwie Server01 do wersji 12,0.</span><span class="sxs-lookup"><span data-stu-id="fc1bc-117">The final command upgrades the existing server named Server01 to version 12.0.</span></span>
<span data-ttu-id="fc1bc-118">Najwcześniejszym momentem uaktualnienia jest pięć minut po uruchomieniu polecenia zgodnie z określoną zmienną $ScheduleTime.</span><span class="sxs-lookup"><span data-stu-id="fc1bc-118">The earliest time to upgrade is five minutes after you run the command, as specified by the $ScheduleTime variable.</span></span>
<span data-ttu-id="fc1bc-119">Po uaktualnieniu baza danych ContosoDB będzie działać w wersji Standard i mieć zamierzenie poziomu usługi S0.</span><span class="sxs-lookup"><span data-stu-id="fc1bc-119">After the upgrade, the database contosodb will be running the Standard edition and have the Service Level Objective S0.</span></span>

## <span data-ttu-id="fc1bc-120">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="fc1bc-120">PARAMETERS</span></span>

### <span data-ttu-id="fc1bc-121">-DatabaseCollection</span><span class="sxs-lookup"><span data-stu-id="fc1bc-121">-DatabaseCollection</span></span>
<span data-ttu-id="fc1bc-122">Określa tablicę obiektów **RecommendedDatabaseProperties** , których używa polecenie cmdlet w celu uaktualnienia serwera.</span><span class="sxs-lookup"><span data-stu-id="fc1bc-122">Specifies an array of **RecommendedDatabaseProperties** objects that this cmdlet uses for the server upgrade.</span></span>

```yaml
Type: Microsoft.Azure.Management.Sql.LegacySdk.Models.RecommendedDatabaseProperties[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fc1bc-123">-ElasticPoolCollection</span><span class="sxs-lookup"><span data-stu-id="fc1bc-123">-ElasticPoolCollection</span></span>
<span data-ttu-id="fc1bc-124">Określa tablicę obiektów **UpgradeRecommendedElasticPoolProperties** , których należy użyć w celu uaktualnienia serwera.</span><span class="sxs-lookup"><span data-stu-id="fc1bc-124">Specifies an array of **UpgradeRecommendedElasticPoolProperties** objects to use for the server upgrade.</span></span>

```yaml
Type: Microsoft.Azure.Management.Sql.LegacySdk.Models.UpgradeRecommendedElasticPoolProperties[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fc1bc-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fc1bc-125">-ResourceGroupName</span></span>
<span data-ttu-id="fc1bc-126">Określa nazwę grupy zasobów, do której jest przypisany serwer.</span><span class="sxs-lookup"><span data-stu-id="fc1bc-126">Specifies the name of the resource group to which the server is assigned.</span></span>

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

### <span data-ttu-id="fc1bc-127">-ScheduleUpgradeAfterUtcDateTime</span><span class="sxs-lookup"><span data-stu-id="fc1bc-127">-ScheduleUpgradeAfterUtcDateTime</span></span>
<span data-ttu-id="fc1bc-128">Określa najwcześniejszą godzinę, jako obiekt **DateTime** , do uaktualnienia serwera.</span><span class="sxs-lookup"><span data-stu-id="fc1bc-128">Specifies the earliest time, as a **DateTime** object, to upgrade the server.</span></span>
<span data-ttu-id="fc1bc-129">Określ wartość w formacie ISO8601, wyrażoną jako uniwersalny czas koordynowany (UTC).</span><span class="sxs-lookup"><span data-stu-id="fc1bc-129">Specify a value in the ISO8601 format, in Coordinated Universal Time (UTC).</span></span>
<span data-ttu-id="fc1bc-130">Aby uzyskać więcej informacji, wpisz tekst `Get-Help Get-Date` .</span><span class="sxs-lookup"><span data-stu-id="fc1bc-130">For more information, type `Get-Help Get-Date`.</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fc1bc-131">-Nazwa_serwera</span><span class="sxs-lookup"><span data-stu-id="fc1bc-131">-ServerName</span></span>
<span data-ttu-id="fc1bc-132">Określa nazwę serwera, który jest uaktualniany przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fc1bc-132">Specifies the name of the server that this cmdlet upgrades.</span></span>

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

### <span data-ttu-id="fc1bc-133">-ServerVersion</span><span class="sxs-lookup"><span data-stu-id="fc1bc-133">-ServerVersion</span></span>
<span data-ttu-id="fc1bc-134">Określa wersję, z którą to polecenie cmdlet uaktualnia serwer.</span><span class="sxs-lookup"><span data-stu-id="fc1bc-134">Specifies the version to which this cmdlet upgrades the server.</span></span>
<span data-ttu-id="fc1bc-135">Jedyną prawidłową wartością jest 12,0.</span><span class="sxs-lookup"><span data-stu-id="fc1bc-135">The only valid value is 12.0.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fc1bc-136">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fc1bc-136">-DefaultProfile</span></span>
<span data-ttu-id="fc1bc-137">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="fc1bc-137">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fc1bc-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fc1bc-138">CommonParameters</span></span>
<span data-ttu-id="fc1bc-139">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fc1bc-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fc1bc-140">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fc1bc-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fc1bc-141">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="fc1bc-141">INPUTS</span></span>

## <span data-ttu-id="fc1bc-142">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="fc1bc-142">OUTPUTS</span></span>

### <span data-ttu-id="fc1bc-143">Microsoft. Azure. Commands. SQL. ServerUpgrade. model. AzureSqlServerUpgradeModel</span><span class="sxs-lookup"><span data-stu-id="fc1bc-143">Microsoft.Azure.Commands.Sql.ServerUpgrade.Model.AzureSqlServerUpgradeModel</span></span>

## <span data-ttu-id="fc1bc-144">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="fc1bc-144">NOTES</span></span>

## <span data-ttu-id="fc1bc-145">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="fc1bc-145">RELATED LINKS</span></span>

[<span data-ttu-id="fc1bc-146">Get-AzureRmSqlServerUpgrade</span><span class="sxs-lookup"><span data-stu-id="fc1bc-146">Get-AzureRmSqlServerUpgrade</span></span>](./Get-AzureRmSqlServerUpgrade.md)

[<span data-ttu-id="fc1bc-147">Zatrzymaj — AzureRmSqlServerUpgrade</span><span class="sxs-lookup"><span data-stu-id="fc1bc-147">Stop-AzureRmSqlServerUpgrade</span></span>](./Stop-AzureRmSqlServerUpgrade.md)

[<span data-ttu-id="fc1bc-148">Dokumentacja bazy danych SQL</span><span class="sxs-lookup"><span data-stu-id="fc1bc-148">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


