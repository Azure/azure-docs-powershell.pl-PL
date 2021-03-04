---
external help file: Microsoft.Azure.PowerShell.Cmdlets.AnalysisServices.Dataplane.dll-Help.xml
Module Name: Az.AnalysisServices
online version: https://docs.microsoft.com/powershell/module/az.analysisservices/sync-azanalysisservicesinstance
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AnalysisServices/AnalysisServices/help/Sync-AzAnalysisServicesInstance.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AnalysisServices/AnalysisServices/help/Sync-AzAnalysisServicesInstance.md
ms.openlocfilehash: c5ffd95cb3bd5e902e2e9edadfa9c96dd441c744
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101959226"
---
# <span data-ttu-id="b2bb4-101">Sync-AzAnalysisServicesInstance</span><span class="sxs-lookup"><span data-stu-id="b2bb4-101">Sync-AzAnalysisServicesInstance</span></span>

## <span data-ttu-id="b2bb4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b2bb4-102">SYNOPSIS</span></span>

<span data-ttu-id="b2bb4-103">Synchronizuje określoną bazę danych na określonym wystąpieniu serwera usług Analysis Services ze wszystkimi wystąpieniami skalowania zapytania w obecnie zalogowanym środowisku zgodnie z Add-AzAnalysisServicesAccount polecenia</span><span class="sxs-lookup"><span data-stu-id="b2bb4-103">Synchronizes a specified database on the specified instance of Analysis Services server to all the query scaleout instances in the currently logged in Environment as specified in Add-AzAnalysisServicesAccount command</span></span>

## <span data-ttu-id="b2bb4-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="b2bb4-104">SYNTAX</span></span>

```
Sync-AzAnalysisServicesInstance [-Database] <String> [-Instance] <String> [-PassThru] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="b2bb4-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="b2bb4-105">DESCRIPTION</span></span>

<span data-ttu-id="b2bb4-106">Polecenie cmdlet Sync-AzAnalysisServicesInstance synchronizuje określoną bazę danych w określonym wystąpieniu serwera usług Analysis Services ze wszystkimi wystąpieniami skalowania zapytania w obecnie zalogowanym środowisku zgodnie z poleceniem Add-AzAnalysisServicesAccount</span><span class="sxs-lookup"><span data-stu-id="b2bb4-106">The Sync-AzAnalysisServicesInstance cmdlet synchronizes a specified database on the specified instance of Analysis Services server to all the query scaleout instances in the currently logged in Environment as specified in Add-AzAnalysisServicesAccount command</span></span>

## <span data-ttu-id="b2bb4-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="b2bb4-107">EXAMPLES</span></span>

### <span data-ttu-id="b2bb4-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="b2bb4-108">Example 1</span></span>

```
PS C:\>Sync-AzAnalysisServicesInstance -Instance asazure://westus.asazure.windows.net/contoso -Database SalesOrders
```

<span data-ttu-id="b2bb4-109">To polecenie zsynchronizuje bazę danych o nazwie ZamówieniaSprzedaży na serwerze o nazwie "contoso" w środowisku westus.asazure.windows.net pod warunkiem, że użytkownik zalogował się do tego środowiska przy użyciu Add-AzAnalysisServicesAccount użytkownika.</span><span class="sxs-lookup"><span data-stu-id="b2bb4-109">This command will synchronize the database named SalesOrders in the server named 'contoso' in the environment westus.asazure.windows.net provided the user has logged-in to this environment using Add-AzAnalysisServicesAccount command.</span></span>

## <span data-ttu-id="b2bb4-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b2bb4-110">PARAMETERS</span></span>

### <span data-ttu-id="b2bb4-111">— Baza danych</span><span class="sxs-lookup"><span data-stu-id="b2bb4-111">-Database</span></span>

<span data-ttu-id="b2bb4-112">Tożsamość bazy danych do zsynchronizowania</span><span class="sxs-lookup"><span data-stu-id="b2bb4-112">Identity of the database to be synchronized</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b2bb4-113">—Instance</span><span class="sxs-lookup"><span data-stu-id="b2bb4-113">-Instance</span></span>

<span data-ttu-id="b2bb4-114">Nazwa wystąpienia serwera usług Analysis Services do ponownego uruchomienia</span><span class="sxs-lookup"><span data-stu-id="b2bb4-114">Name of the Analysis Services server instance to restart</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b2bb4-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b2bb4-115">-PassThru</span></span>

<span data-ttu-id="b2bb4-116">Określenie tej wartości spowoduje zwrócenie wartości prawda, jeśli polecenie zostało pomyślnie określone.</span><span class="sxs-lookup"><span data-stu-id="b2bb4-116">Specifying this will return true if the command was successful.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b2bb4-117">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="b2bb4-117">-Confirm</span></span>
<span data-ttu-id="b2bb4-118">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="b2bb4-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b2bb4-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b2bb4-119">-WhatIf</span></span>
<span data-ttu-id="b2bb4-120">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b2bb4-120">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="b2bb4-121">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="b2bb4-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b2bb4-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b2bb4-122">CommonParameters</span></span>
<span data-ttu-id="b2bb4-123">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b2bb4-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b2bb4-124">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b2bb4-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b2bb4-125">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b2bb4-125">INPUTS</span></span>

### <span data-ttu-id="b2bb4-126">System.String</span><span class="sxs-lookup"><span data-stu-id="b2bb4-126">System.String</span></span>

## <span data-ttu-id="b2bb4-127">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b2bb4-127">OUTPUTS</span></span>

### <span data-ttu-id="b2bb4-128">Microsoft.Azure.Commands.AnalysisServices.Dataplane.Models.ScaleOutServerDatabaseSyncDetails</span><span class="sxs-lookup"><span data-stu-id="b2bb4-128">Microsoft.Azure.Commands.AnalysisServices.Dataplane.Models.ScaleOutServerDatabaseSyncDetails</span></span>

## <span data-ttu-id="b2bb4-129">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="b2bb4-129">NOTES</span></span>

<span data-ttu-id="b2bb4-130">Alias: Sync-AzAsInstance</span><span class="sxs-lookup"><span data-stu-id="b2bb4-130">Alias: Sync-AzAsInstance</span></span>

## <span data-ttu-id="b2bb4-131">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="b2bb4-131">RELATED LINKS</span></span>
