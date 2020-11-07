---
external help file: Microsoft.Azure.PowerShell.Cmdlets.AnalysisServices.Dataplane.dll-Help.xml
Module Name: Az.AnalysisServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.analysisservices/sync-azanalysisservicesinstance
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AnalysisServices/AnalysisServices/help/Sync-AzAnalysisServicesInstance.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AnalysisServices/AnalysisServices/help/Sync-AzAnalysisServicesInstance.md
ms.openlocfilehash: ad56d44912b38cc5af7794b909b2fb009eca0aa9
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93704685"
---
# <span data-ttu-id="aa991-101">Sync-AzAnalysisServicesInstance</span><span class="sxs-lookup"><span data-stu-id="aa991-101">Sync-AzAnalysisServicesInstance</span></span>

## <span data-ttu-id="aa991-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="aa991-102">SYNOPSIS</span></span>

<span data-ttu-id="aa991-103">Synchronizuje określoną bazę danych w określonym wystąpieniu serwera usług Analysis Services ze wszystkimi wystąpieniami ScaleOut zapytań w aktualnie zalogowanym środowisku określonym w Add-AzAnalysisServicesAccount polecenia.</span><span class="sxs-lookup"><span data-stu-id="aa991-103">Synchronizes a specified database on the specified instance of Analysis Services server to all the query scaleout instances in the currently logged in Environment as specified in Add-AzAnalysisServicesAccount command</span></span>

## <span data-ttu-id="aa991-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="aa991-104">SYNTAX</span></span>

```
Sync-AzAnalysisServicesInstance [-Database] <String> [-Instance] <String> [-PassThru] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="aa991-105">Opis</span><span class="sxs-lookup"><span data-stu-id="aa991-105">DESCRIPTION</span></span>

<span data-ttu-id="aa991-106">Polecenie cmdlet Sync-AzAnalysisServicesInstance synchronizuje określoną bazę danych w określonym wystąpieniu serwera usług Analysis Services ze wszystkimi wystąpieniami ScaleOut zapytań w obecnie zarejestrowaniu środowisku określonym w Add-AzAnalysisServicesAccount polecenie</span><span class="sxs-lookup"><span data-stu-id="aa991-106">The Sync-AzAnalysisServicesInstance cmdlet synchronizes a specified database on the specified instance of Analysis Services server to all the query scaleout instances in the currently logged in Environment as specified in Add-AzAnalysisServicesAccount command</span></span>

## <span data-ttu-id="aa991-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="aa991-107">EXAMPLES</span></span>

### <span data-ttu-id="aa991-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="aa991-108">Example 1</span></span>

```
PS C:\>Sync-AzAnalysisServicesInstance -Instance asazure://westus.asazure.windows.net/contoso -Database SalesOrders
```

<span data-ttu-id="aa991-109">To polecenie zsynchronizuje bazę danych o nazwie SalesOrders na serwerze o nazwie "contoso" w westus.asazure.windows.net środowiska, pod warunkiem że użytkownik zarejestrował się do tego środowiska przy użyciu Add-AzAnalysisServicesAccount polecenia.</span><span class="sxs-lookup"><span data-stu-id="aa991-109">This command will synchronize the database named SalesOrders in the server named 'contoso' in the environment westus.asazure.windows.net provided the user has logged-in to this enviroment using Add-AzAnalysisServicesAccount command.</span></span>

## <span data-ttu-id="aa991-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="aa991-110">PARAMETERS</span></span>

### <span data-ttu-id="aa991-111">-Database</span><span class="sxs-lookup"><span data-stu-id="aa991-111">-Database</span></span>

<span data-ttu-id="aa991-112">Tożsamość bazy danych do zsynchronizowania</span><span class="sxs-lookup"><span data-stu-id="aa991-112">Identity of the database to be synchronized</span></span>

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

### <span data-ttu-id="aa991-113">-Instance</span><span class="sxs-lookup"><span data-stu-id="aa991-113">-Instance</span></span>

<span data-ttu-id="aa991-114">Nazwa wystąpienia serwera usług Analysis Services do ponownego uruchomienia</span><span class="sxs-lookup"><span data-stu-id="aa991-114">Name of the Analysis Services server instance to restart</span></span>

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

### <span data-ttu-id="aa991-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="aa991-115">-PassThru</span></span>

<span data-ttu-id="aa991-116">Określenie tej wartości zwróci wartość PRAWDA, jeśli polecenie zostało wykonane prawidłowo.</span><span class="sxs-lookup"><span data-stu-id="aa991-116">Specifying this will return true if the command was successful.</span></span>

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

### <span data-ttu-id="aa991-117">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="aa991-117">-Confirm</span></span>
<span data-ttu-id="aa991-118">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="aa991-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="aa991-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="aa991-119">-WhatIf</span></span>
<span data-ttu-id="aa991-120">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="aa991-120">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="aa991-121">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="aa991-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="aa991-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aa991-122">CommonParameters</span></span>
<span data-ttu-id="aa991-123">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="aa991-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aa991-124">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="aa991-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aa991-125">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="aa991-125">INPUTS</span></span>

### <span data-ttu-id="aa991-126">System. String</span><span class="sxs-lookup"><span data-stu-id="aa991-126">System.String</span></span>

## <span data-ttu-id="aa991-127">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="aa991-127">OUTPUTS</span></span>

### <span data-ttu-id="aa991-128">Microsoft. Azure. Commands. AnalysisServices. dataplan. models. ScaleOutServerDatabaseSyncDetails</span><span class="sxs-lookup"><span data-stu-id="aa991-128">Microsoft.Azure.Commands.AnalysisServices.Dataplane.Models.ScaleOutServerDatabaseSyncDetails</span></span>

## <span data-ttu-id="aa991-129">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="aa991-129">NOTES</span></span>

<span data-ttu-id="aa991-130">Alias: Sync-AzAsInstance</span><span class="sxs-lookup"><span data-stu-id="aa991-130">Alias: Sync-AzAsInstance</span></span>

## <span data-ttu-id="aa991-131">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="aa991-131">RELATED LINKS</span></span>
