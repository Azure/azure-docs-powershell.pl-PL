---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/Get-AzSqlInstanceDatabaseLogReplay
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlInstanceDatabaseLogReplay.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlInstanceDatabaseLogReplay.md
ms.openlocfilehash: 7e37dcceb45370e4956fb59912a50a501fe271c1
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/27/2020
ms.locfileid: "94233839"
---
# <span data-ttu-id="9ebf0-101">Get-AzSqlInstanceDatabaseLogReplay</span><span class="sxs-lookup"><span data-stu-id="9ebf0-101">Get-AzSqlInstanceDatabaseLogReplay</span></span>

## <span data-ttu-id="9ebf0-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="9ebf0-102">SYNOPSIS</span></span>
<span data-ttu-id="9ebf0-103">Pobiera stan usługi powtarzania dziennika.</span><span class="sxs-lookup"><span data-stu-id="9ebf0-103">Gets the Log Replay service status.</span></span>

## <span data-ttu-id="9ebf0-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="9ebf0-104">SYNTAX</span></span>

```
Get-AzSqlInstanceDatabaseLogReplay [[-Name] <String>] [-InstanceName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9ebf0-105">Opis</span><span class="sxs-lookup"><span data-stu-id="9ebf0-105">DESCRIPTION</span></span>
<span data-ttu-id="9ebf0-106">Polecenie cmdlet **Get-AzSqlInstanceDatabaseLogReplay** Pobiera stan usługa powtarzania dziennika w danej bazie danych.</span><span class="sxs-lookup"><span data-stu-id="9ebf0-106">The **Get-AzSqlInstanceDatabaseLogReplay** cmdlet gets the Log Replay service status on the given database.</span></span>

## <span data-ttu-id="9ebf0-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="9ebf0-107">EXAMPLES</span></span>

### <span data-ttu-id="9ebf0-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="9ebf0-108">Example 1</span></span>
```powershell
PS C:\> Get-AzSqlInstanceDatabaseLogReplay -ResourceGroupName "ResourceGroup01" -InstanceName "ManagedInstance01" -Name "ManagedDatabaseName"
```

<span data-ttu-id="9ebf0-109">To polecenie spowoduje wyświetlenie stanu usługi powtarzania dziennika w danej bazie danych.</span><span class="sxs-lookup"><span data-stu-id="9ebf0-109">This command will get log replay service status on the given database.</span></span>

## <span data-ttu-id="9ebf0-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="9ebf0-110">PARAMETERS</span></span>

### <span data-ttu-id="9ebf0-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9ebf0-111">-DefaultProfile</span></span>
<span data-ttu-id="9ebf0-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="9ebf0-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9ebf0-113">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="9ebf0-113">-InstanceName</span></span>
<span data-ttu-id="9ebf0-114">Nazwa wystąpienia.</span><span class="sxs-lookup"><span data-stu-id="9ebf0-114">The name of the instance.</span></span>

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

### <span data-ttu-id="9ebf0-115">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="9ebf0-115">-Name</span></span>
<span data-ttu-id="9ebf0-116">Nazwa bazy danych wystąpienia do pobrania.</span><span class="sxs-lookup"><span data-stu-id="9ebf0-116">The name of the instance database to retrieve.</span></span>

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

### <span data-ttu-id="9ebf0-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9ebf0-117">-ResourceGroupName</span></span>
<span data-ttu-id="9ebf0-118">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="9ebf0-118">The name of the resource group.</span></span>

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

### <span data-ttu-id="9ebf0-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9ebf0-119">CommonParameters</span></span>
<span data-ttu-id="9ebf0-120">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9ebf0-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9ebf0-121">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="9ebf0-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9ebf0-122">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="9ebf0-122">INPUTS</span></span>

### <span data-ttu-id="9ebf0-123">System. String</span><span class="sxs-lookup"><span data-stu-id="9ebf0-123">System.String</span></span>

## <span data-ttu-id="9ebf0-124">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="9ebf0-124">OUTPUTS</span></span>

### <span data-ttu-id="9ebf0-125">Microsoft. Azure. Commands. SQL. ManagedDatabase. model. AzureSqlManagedDatabaseRestoreDetailsResultModel</span><span class="sxs-lookup"><span data-stu-id="9ebf0-125">Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlManagedDatabaseRestoreDetailsResultModel</span></span>

## <span data-ttu-id="9ebf0-126">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="9ebf0-126">NOTES</span></span>

## <span data-ttu-id="9ebf0-127">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="9ebf0-127">RELATED LINKS</span></span>
