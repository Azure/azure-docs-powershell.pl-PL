---
external help file: Microsoft.Azure.Commands.AnalysisServices.Dataplane.dll-Help.xml
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.analysisservices/sync-azureanalysisservicesinstance
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AnalysisServices/Commands.AnalysisServices.Dataplane/help/Sync-AzureAnalysisServicesInstance.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AnalysisServices/Commands.AnalysisServices.Dataplane/help/Sync-AzureAnalysisServicesInstance.md
ms.openlocfilehash: f3fb2377fd78db4b330afd39a8691f958597f07a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93528158"
---
# <span data-ttu-id="28c28-101">Sync-AzureAnalysisServicesInstance</span><span class="sxs-lookup"><span data-stu-id="28c28-101">Sync-AzureAnalysisServicesInstance</span></span>

## <span data-ttu-id="28c28-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="28c28-102">SYNOPSIS</span></span>

<span data-ttu-id="28c28-103">Synchronizuje określoną bazę danych w określonym wystąpieniu serwera usług Analysis Services ze wszystkimi wystąpieniami ScaleOut zapytań w aktualnie zalogowanym środowisku określonym w Add-AzureAnalysisServicesAccount polecenia.</span><span class="sxs-lookup"><span data-stu-id="28c28-103">Synchronizes a specified database on the specified instance of Analysis Services server to all the query scaleout instances in the currently logged in Environment as specified in Add-AzureAnalysisServicesAccount command</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="28c28-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="28c28-104">SYNTAX</span></span>

```
Sync-AzureAnalysisServicesInstance [-Instance] <String> [-Database] <String> [-Passthru]
```

## <span data-ttu-id="28c28-105">Opis</span><span class="sxs-lookup"><span data-stu-id="28c28-105">DESCRIPTION</span></span>

<span data-ttu-id="28c28-106">Polecenie cmdlet Sync-AzureAnalysisServicesInstance synchronizuje określoną bazę danych w określonym wystąpieniu serwera usług Analysis Services ze wszystkimi wystąpieniami ScaleOut zapytań w obecnie zarejestrowaniu środowisku określonym w Add-AzureAnalysisServicesAccount polecenie</span><span class="sxs-lookup"><span data-stu-id="28c28-106">The Sync-AzureAnalysisServicesInstance cmdlet synchronizes a specified database on the specified instance of Analysis Services server to all the query scaleout instances in the currently logged in Environment as specified in Add-AzureAnalysisServicesAccount command</span></span>

## <span data-ttu-id="28c28-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="28c28-107">EXAMPLES</span></span>

### <span data-ttu-id="28c28-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="28c28-108">Example 1</span></span>

```
PS C:\>Sync-AzureAnalysisServicesInstance -Instance asazure://westus.asazure.windows.net/contoso -Database SalesOrders
```

<span data-ttu-id="28c28-109">To polecenie zsynchronizuje bazę danych o nazwie SalesOrders na serwerze o nazwie "contoso" w westus.asazure.windows.net środowiska, pod warunkiem że użytkownik zarejestrował się do tego środowiska przy użyciu Add-AzureAnalysisServicesAccount polecenia.</span><span class="sxs-lookup"><span data-stu-id="28c28-109">This command will synchronize the database named SalesOrders in the server named 'contoso' in the environment westus.asazure.windows.net provided the user has logged-in to this enviroment using Add-AzureAnalysisServicesAccount command.</span></span>

## <span data-ttu-id="28c28-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="28c28-110">PARAMETERS</span></span>

### <span data-ttu-id="28c28-111">-Instance</span><span class="sxs-lookup"><span data-stu-id="28c28-111">-Instance</span></span>

<span data-ttu-id="28c28-112">Nazwa wystąpienia serwera usług Analysis Services do ponownego uruchomienia</span><span class="sxs-lookup"><span data-stu-id="28c28-112">Name of the Analysis Services server instance to restart</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="28c28-113">-Database</span><span class="sxs-lookup"><span data-stu-id="28c28-113">-Database</span></span>

<span data-ttu-id="28c28-114">Tożsamość bazy danych do zsynchronizowania</span><span class="sxs-lookup"><span data-stu-id="28c28-114">Identity of the database to be synchronized</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="28c28-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="28c28-115">-PassThru</span></span>

<span data-ttu-id="28c28-116">Określenie tej wartości zwróci wartość PRAWDA, jeśli polecenie zostało wykonane prawidłowo.</span><span class="sxs-lookup"><span data-stu-id="28c28-116">Specifying this will return true if the command was successful.</span></span>

```yaml
Type: Switch
Parameter Sets: (All)
Aliases: 
Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

## <span data-ttu-id="28c28-117">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="28c28-117">INPUTS</span></span>

### <span data-ttu-id="28c28-118">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="28c28-118">None</span></span>
<span data-ttu-id="28c28-119">To polecenie cmdlet nie akceptuje żadnych danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="28c28-119">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="28c28-120">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="28c28-120">OUTPUTS</span></span>

### <span data-ttu-id="28c28-121">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="28c28-121">System.Boolean</span></span>

## <span data-ttu-id="28c28-122">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="28c28-122">NOTES</span></span>

<span data-ttu-id="28c28-123">Alias: Sync-AzureAsInstance</span><span class="sxs-lookup"><span data-stu-id="28c28-123">Alias: Sync-AzureAsInstance</span></span>

## <span data-ttu-id="28c28-124">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="28c28-124">RELATED LINKS</span></span>
