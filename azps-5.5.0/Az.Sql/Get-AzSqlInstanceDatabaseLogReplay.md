---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/Get-AzSqlInstanceDatabaseLogReplay
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlInstanceDatabaseLogReplay.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlInstanceDatabaseLogReplay.md
ms.openlocfilehash: 7e37dcceb45370e4956fb59912a50a501fe271c1
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100198563"
---
# <span data-ttu-id="785fb-101">Get-AzSqlInstanceDatabaseLogReplay</span><span class="sxs-lookup"><span data-stu-id="785fb-101">Get-AzSqlInstanceDatabaseLogReplay</span></span>

## <span data-ttu-id="785fb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="785fb-102">SYNOPSIS</span></span>
<span data-ttu-id="785fb-103">Pobiera stan usługi ponownego odtwarzania dziennika.</span><span class="sxs-lookup"><span data-stu-id="785fb-103">Gets the Log Replay service status.</span></span>

## <span data-ttu-id="785fb-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="785fb-104">SYNTAX</span></span>

```
Get-AzSqlInstanceDatabaseLogReplay [[-Name] <String>] [-InstanceName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="785fb-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="785fb-105">DESCRIPTION</span></span>
<span data-ttu-id="785fb-106">Polecenie **cmdlet Get-AzSqlInstanceDatabaseLogReplay** pobiera stan usługi Odtwarzanie dziennika w danej bazie danych.</span><span class="sxs-lookup"><span data-stu-id="785fb-106">The **Get-AzSqlInstanceDatabaseLogReplay** cmdlet gets the Log Replay service status on the given database.</span></span>

## <span data-ttu-id="785fb-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="785fb-107">EXAMPLES</span></span>

### <span data-ttu-id="785fb-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="785fb-108">Example 1</span></span>
```powershell
PS C:\> Get-AzSqlInstanceDatabaseLogReplay -ResourceGroupName "ResourceGroup01" -InstanceName "ManagedInstance01" -Name "ManagedDatabaseName"
```

<span data-ttu-id="785fb-109">To polecenie spowoduje stan usługi ponownego odtwarzania dziennika w danej bazie danych.</span><span class="sxs-lookup"><span data-stu-id="785fb-109">This command will get log replay service status on the given database.</span></span>

## <span data-ttu-id="785fb-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="785fb-110">PARAMETERS</span></span>

### <span data-ttu-id="785fb-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="785fb-111">-DefaultProfile</span></span>
<span data-ttu-id="785fb-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="785fb-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="785fb-113">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="785fb-113">-InstanceName</span></span>
<span data-ttu-id="785fb-114">Nazwa wystąpienia.</span><span class="sxs-lookup"><span data-stu-id="785fb-114">The name of the instance.</span></span>

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

### <span data-ttu-id="785fb-115">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="785fb-115">-Name</span></span>
<span data-ttu-id="785fb-116">Nazwa wystąpienia bazy danych do pobrania.</span><span class="sxs-lookup"><span data-stu-id="785fb-116">The name of the instance database to retrieve.</span></span>

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

### <span data-ttu-id="785fb-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="785fb-117">-ResourceGroupName</span></span>
<span data-ttu-id="785fb-118">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="785fb-118">The name of the resource group.</span></span>

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

### <span data-ttu-id="785fb-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="785fb-119">CommonParameters</span></span>
<span data-ttu-id="785fb-120">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="785fb-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="785fb-121">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="785fb-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="785fb-122">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="785fb-122">INPUTS</span></span>

### <span data-ttu-id="785fb-123">System.String</span><span class="sxs-lookup"><span data-stu-id="785fb-123">System.String</span></span>

## <span data-ttu-id="785fb-124">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="785fb-124">OUTPUTS</span></span>

### <span data-ttu-id="785fb-125">Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlManagedDatabaseRestoreDetailsResultModel</span><span class="sxs-lookup"><span data-stu-id="785fb-125">Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlManagedDatabaseRestoreDetailsResultModel</span></span>

## <span data-ttu-id="785fb-126">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="785fb-126">NOTES</span></span>

## <span data-ttu-id="785fb-127">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="785fb-127">RELATED LINKS</span></span>
