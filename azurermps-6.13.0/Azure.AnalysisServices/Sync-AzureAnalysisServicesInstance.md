---
external help file: Microsoft.Azure.Commands.AnalysisServices.Dataplane.dll-Help.xml
Module Name: Azure.AnalysisServices
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.analysisservices/sync-azureanalysisservicesinstance
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AnalysisServices/Commands.AnalysisServices.Dataplane/help/Sync-AzureAnalysisServicesInstance.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AnalysisServices/Commands.AnalysisServices.Dataplane/help/Sync-AzureAnalysisServicesInstance.md
ms.openlocfilehash: 732eb92a46fa7e69ba5274398de648c16142ae75
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93526461"
---
# <span data-ttu-id="2f9b6-101">Sync-AzureAnalysisServicesInstance</span><span class="sxs-lookup"><span data-stu-id="2f9b6-101">Sync-AzureAnalysisServicesInstance</span></span>

## <span data-ttu-id="2f9b6-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="2f9b6-102">SYNOPSIS</span></span>

<span data-ttu-id="2f9b6-103">Synchronizuje określoną bazę danych w określonym wystąpieniu serwera usług Analysis Services ze wszystkimi wystąpieniami ScaleOut zapytań w aktualnie zalogowanym środowisku określonym w Add-AzureAnalysisServicesAccount polecenia.</span><span class="sxs-lookup"><span data-stu-id="2f9b6-103">Synchronizes a specified database on the specified instance of Analysis Services server to all the query scaleout instances in the currently logged in Environment as specified in Add-AzureAnalysisServicesAccount command</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2f9b6-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="2f9b6-104">SYNTAX</span></span>

```
Sync-AzureAnalysisServicesInstance [-Instance] <String> [-Database] <String> [-PassThru] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="2f9b6-105">Opis</span><span class="sxs-lookup"><span data-stu-id="2f9b6-105">DESCRIPTION</span></span>

<span data-ttu-id="2f9b6-106">Polecenie cmdlet Sync-AzureAnalysisServicesInstance synchronizuje określoną bazę danych w określonym wystąpieniu serwera usług Analysis Services ze wszystkimi wystąpieniami ScaleOut zapytań w obecnie zarejestrowaniu środowisku określonym w Add-AzureAnalysisServicesAccount polecenie</span><span class="sxs-lookup"><span data-stu-id="2f9b6-106">The Sync-AzureAnalysisServicesInstance cmdlet synchronizes a specified database on the specified instance of Analysis Services server to all the query scaleout instances in the currently logged in Environment as specified in Add-AzureAnalysisServicesAccount command</span></span>

## <span data-ttu-id="2f9b6-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="2f9b6-107">EXAMPLES</span></span>

### <span data-ttu-id="2f9b6-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="2f9b6-108">Example 1</span></span>

```
PS C:\>Sync-AzureAnalysisServicesInstance -Instance asazure://westus.asazure.windows.net/contoso -Database SalesOrders
```

<span data-ttu-id="2f9b6-109">To polecenie zsynchronizuje bazę danych o nazwie SalesOrders na serwerze o nazwie "contoso" w westus.asazure.windows.net środowiska, pod warunkiem że użytkownik zarejestrował się do tego środowiska przy użyciu Add-AzureAnalysisServicesAccount polecenia.</span><span class="sxs-lookup"><span data-stu-id="2f9b6-109">This command will synchronize the database named SalesOrders in the server named 'contoso' in the environment westus.asazure.windows.net provided the user has logged-in to this enviroment using Add-AzureAnalysisServicesAccount command.</span></span>

## <span data-ttu-id="2f9b6-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="2f9b6-110">PARAMETERS</span></span>

### <span data-ttu-id="2f9b6-111">-Database</span><span class="sxs-lookup"><span data-stu-id="2f9b6-111">-Database</span></span>

<span data-ttu-id="2f9b6-112">Tożsamość bazy danych do zsynchronizowania</span><span class="sxs-lookup"><span data-stu-id="2f9b6-112">Identity of the database to be synchronized</span></span>

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

### <span data-ttu-id="2f9b6-113">-Instance</span><span class="sxs-lookup"><span data-stu-id="2f9b6-113">-Instance</span></span>

<span data-ttu-id="2f9b6-114">Nazwa wystąpienia serwera usług Analysis Services do ponownego uruchomienia</span><span class="sxs-lookup"><span data-stu-id="2f9b6-114">Name of the Analysis Services server instance to restart</span></span>

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

### <span data-ttu-id="2f9b6-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="2f9b6-115">-PassThru</span></span>

<span data-ttu-id="2f9b6-116">Określenie tej wartości zwróci wartość PRAWDA, jeśli polecenie zostało wykonane prawidłowo.</span><span class="sxs-lookup"><span data-stu-id="2f9b6-116">Specifying this will return true if the command was successful.</span></span>

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

### <span data-ttu-id="2f9b6-117">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="2f9b6-117">-Confirm</span></span>
<span data-ttu-id="2f9b6-118">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2f9b6-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2f9b6-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2f9b6-119">-WhatIf</span></span>
<span data-ttu-id="2f9b6-120">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2f9b6-120">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="2f9b6-121">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="2f9b6-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2f9b6-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2f9b6-122">CommonParameters</span></span>
<span data-ttu-id="2f9b6-123">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2f9b6-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2f9b6-124">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2f9b6-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2f9b6-125">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="2f9b6-125">INPUTS</span></span>

### <span data-ttu-id="2f9b6-126">System. String</span><span class="sxs-lookup"><span data-stu-id="2f9b6-126">System.String</span></span>
<span data-ttu-id="2f9b6-127">Parametry: Database (ByValue), Instance (ByValue)</span><span class="sxs-lookup"><span data-stu-id="2f9b6-127">Parameters: Database (ByValue), Instance (ByValue)</span></span>

## <span data-ttu-id="2f9b6-128">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="2f9b6-128">OUTPUTS</span></span>

### <span data-ttu-id="2f9b6-129">Microsoft. Azure. Commands. AnalysisServices. dataplan. models. ScaleOutServerDatabaseSyncDetails</span><span class="sxs-lookup"><span data-stu-id="2f9b6-129">Microsoft.Azure.Commands.AnalysisServices.Dataplane.Models.ScaleOutServerDatabaseSyncDetails</span></span>

## <span data-ttu-id="2f9b6-130">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="2f9b6-130">NOTES</span></span>

<span data-ttu-id="2f9b6-131">Alias: Sync-AzureAsInstance</span><span class="sxs-lookup"><span data-stu-id="2f9b6-131">Alias: Sync-AzureAsInstance</span></span>

## <span data-ttu-id="2f9b6-132">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="2f9b6-132">RELATED LINKS</span></span>
