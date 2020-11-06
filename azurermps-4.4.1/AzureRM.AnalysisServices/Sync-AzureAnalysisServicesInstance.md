---
external help file: Microsoft.Azure.Commands.AnalysisServices.Dataplane.dll-Help.xml
Module Name: Azure.AnalysisServices
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AnalysisServices/Commands.AnalysisServices.Dataplane/help/Sync-AzureAnalysisServicesInstance.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AnalysisServices/Commands.AnalysisServices.Dataplane/help/Sync-AzureAnalysisServicesInstance.md
ms.openlocfilehash: a75ae79722fed99ce96b0a082f4f56ace998354e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93527750"
---
# <span data-ttu-id="85e7a-101">Sync-AzureAnalysisServicesInstance</span><span class="sxs-lookup"><span data-stu-id="85e7a-101">Sync-AzureAnalysisServicesInstance</span></span>

## <span data-ttu-id="85e7a-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="85e7a-102">SYNOPSIS</span></span>
<span data-ttu-id="85e7a-103">Synchronizuje określoną bazę danych w określonym wystąpieniu serwera usług Analysis Services ze wszystkimi wystąpieniami ScaleOut zapytań w aktualnie zalogowanym środowisku określonym w Add-AzureAnalysisServicesAccount polecenia.</span><span class="sxs-lookup"><span data-stu-id="85e7a-103">Synchronizes a specified database on the specified instance of Analysis Services server to all the query scaleout instances in the currently logged in Environment as specified in Add-AzureAnalysisServicesAccount command</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="85e7a-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="85e7a-104">SYNTAX</span></span>

```
Sync-AzureAnalysisServicesInstance [-Instance] <String> [-Database] <String> [-PassThru] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="85e7a-105">Opis</span><span class="sxs-lookup"><span data-stu-id="85e7a-105">DESCRIPTION</span></span>
<span data-ttu-id="85e7a-106">Polecenie cmdlet Sync-AzureAnalysisServicesInstance synchronizuje określoną bazę danych w określonym wystąpieniu serwera usług Analysis Services ze wszystkimi wystąpieniami ScaleOut zapytań w obecnie zarejestrowaniu środowisku określonym w Add-AzureAnalysisServicesAccount polecenie</span><span class="sxs-lookup"><span data-stu-id="85e7a-106">The Sync-AzureAnalysisServicesInstance cmdlet synchronizes a specified database on the specified instance of Analysis Services server to all the query scaleout instances in the currently logged in Environment as specified in Add-AzureAnalysisServicesAccount command</span></span>

## <span data-ttu-id="85e7a-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="85e7a-107">EXAMPLES</span></span>

### <span data-ttu-id="85e7a-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="85e7a-108">Example 1</span></span>
```
PS C:\>Sync-AzureAnalysisServicesInstance -Instance asazure://westus.asazure.windows.net/contoso -Database SalesOrders
```

<span data-ttu-id="85e7a-109">To polecenie zsynchronizuje bazę danych o nazwie SalesOrders na serwerze o nazwie "contoso" w westus.asazure.windows.net środowiska, pod warunkiem że użytkownik zarejestrował się do tego środowiska przy użyciu Add-AzureAnalysisServicesAccount polecenia.</span><span class="sxs-lookup"><span data-stu-id="85e7a-109">This command will synchronize the database named SalesOrders in the server named 'contoso' in the environment westus.asazure.windows.net provided the user has logged-in to this enviroment using Add-AzureAnalysisServicesAccount command.</span></span>

## <span data-ttu-id="85e7a-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="85e7a-110">PARAMETERS</span></span>

### <span data-ttu-id="85e7a-111">-Instance</span><span class="sxs-lookup"><span data-stu-id="85e7a-111">-Instance</span></span>
<span data-ttu-id="85e7a-112">Nazwa wystąpienia serwera usług Analysis Services do ponownego uruchomienia</span><span class="sxs-lookup"><span data-stu-id="85e7a-112">Name of the Analysis Services server instance to restart</span></span>

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

### <span data-ttu-id="85e7a-113">-Database</span><span class="sxs-lookup"><span data-stu-id="85e7a-113">-Database</span></span>
<span data-ttu-id="85e7a-114">Tożsamość bazy danych do zsynchronizowania</span><span class="sxs-lookup"><span data-stu-id="85e7a-114">Identity of the database to be synchronized</span></span>

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

### <span data-ttu-id="85e7a-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="85e7a-115">-PassThru</span></span>
<span data-ttu-id="85e7a-116">Określenie tej wartości zwróci wartość PRAWDA, jeśli polecenie zostało wykonane prawidłowo.</span><span class="sxs-lookup"><span data-stu-id="85e7a-116">Specifying this will return true if the command was successful.</span></span>

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

### <span data-ttu-id="85e7a-117">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="85e7a-117">-Confirm</span></span>
<span data-ttu-id="85e7a-118">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="85e7a-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="85e7a-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="85e7a-119">-WhatIf</span></span>
<span data-ttu-id="85e7a-120">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="85e7a-120">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="85e7a-121">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="85e7a-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="85e7a-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="85e7a-122">CommonParameters</span></span>
<span data-ttu-id="85e7a-123">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="85e7a-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="85e7a-124">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="85e7a-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="85e7a-125">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="85e7a-125">INPUTS</span></span>

## <span data-ttu-id="85e7a-126">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="85e7a-126">OUTPUTS</span></span>

### <span data-ttu-id="85e7a-127">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="85e7a-127">System.Boolean</span></span>

## <span data-ttu-id="85e7a-128">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="85e7a-128">NOTES</span></span>
<span data-ttu-id="85e7a-129">Alias: Sync-AzureAsInstance</span><span class="sxs-lookup"><span data-stu-id="85e7a-129">Alias: Sync-AzureAsInstance</span></span>

## <span data-ttu-id="85e7a-130">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="85e7a-130">RELATED LINKS</span></span>

