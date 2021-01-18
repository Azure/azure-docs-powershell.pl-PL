---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/Get-AzSqlInstanceDatabaseLogReplay
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlInstanceDatabaseLogReplay.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlInstanceDatabaseLogReplay.md
ms.openlocfilehash: 7e37dcceb45370e4956fb59912a50a501fe271c1
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98499842"
---
# <span data-ttu-id="78f65-101">Get-AzSqlInstanceDatabaseLogReplay</span><span class="sxs-lookup"><span data-stu-id="78f65-101">Get-AzSqlInstanceDatabaseLogReplay</span></span>

## <span data-ttu-id="78f65-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="78f65-102">SYNOPSIS</span></span>
<span data-ttu-id="78f65-103">Pobiera stan usługi powtarzania dziennika.</span><span class="sxs-lookup"><span data-stu-id="78f65-103">Gets the Log Replay service status.</span></span>

## <span data-ttu-id="78f65-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="78f65-104">SYNTAX</span></span>

```
Get-AzSqlInstanceDatabaseLogReplay [[-Name] <String>] [-InstanceName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="78f65-105">Opis</span><span class="sxs-lookup"><span data-stu-id="78f65-105">DESCRIPTION</span></span>
<span data-ttu-id="78f65-106">Polecenie cmdlet **Get-AzSqlInstanceDatabaseLogReplay** Pobiera stan usługa powtarzania dziennika w danej bazie danych.</span><span class="sxs-lookup"><span data-stu-id="78f65-106">The **Get-AzSqlInstanceDatabaseLogReplay** cmdlet gets the Log Replay service status on the given database.</span></span>

## <span data-ttu-id="78f65-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="78f65-107">EXAMPLES</span></span>

### <span data-ttu-id="78f65-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="78f65-108">Example 1</span></span>
```powershell
PS C:\> Get-AzSqlInstanceDatabaseLogReplay -ResourceGroupName "ResourceGroup01" -InstanceName "ManagedInstance01" -Name "ManagedDatabaseName"
```

<span data-ttu-id="78f65-109">To polecenie spowoduje wyświetlenie stanu usługi powtarzania dziennika w danej bazie danych.</span><span class="sxs-lookup"><span data-stu-id="78f65-109">This command will get log replay service status on the given database.</span></span>

## <span data-ttu-id="78f65-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="78f65-110">PARAMETERS</span></span>

### <span data-ttu-id="78f65-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="78f65-111">-DefaultProfile</span></span>
<span data-ttu-id="78f65-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="78f65-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="78f65-113">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="78f65-113">-InstanceName</span></span>
<span data-ttu-id="78f65-114">Nazwa wystąpienia.</span><span class="sxs-lookup"><span data-stu-id="78f65-114">The name of the instance.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ManagedInstanceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="78f65-115">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="78f65-115">-Name</span></span>
<span data-ttu-id="78f65-116">Nazwa bazy danych wystąpienia do pobrania.</span><span class="sxs-lookup"><span data-stu-id="78f65-116">The name of the instance database to retrieve.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: InstanceDatabaseName

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="78f65-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="78f65-117">-ResourceGroupName</span></span>
<span data-ttu-id="78f65-118">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="78f65-118">The name of the resource group.</span></span>

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

### <span data-ttu-id="78f65-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="78f65-119">CommonParameters</span></span>
<span data-ttu-id="78f65-120">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="78f65-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="78f65-121">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="78f65-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="78f65-122">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="78f65-122">INPUTS</span></span>

### <span data-ttu-id="78f65-123">System. String</span><span class="sxs-lookup"><span data-stu-id="78f65-123">System.String</span></span>

## <span data-ttu-id="78f65-124">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="78f65-124">OUTPUTS</span></span>

### <span data-ttu-id="78f65-125">Microsoft. Azure. Commands. SQL. ManagedDatabase. model. AzureSqlManagedDatabaseRestoreDetailsResultModel</span><span class="sxs-lookup"><span data-stu-id="78f65-125">Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlManagedDatabaseRestoreDetailsResultModel</span></span>

## <span data-ttu-id="78f65-126">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="78f65-126">NOTES</span></span>

## <span data-ttu-id="78f65-127">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="78f65-127">RELATED LINKS</span></span>
