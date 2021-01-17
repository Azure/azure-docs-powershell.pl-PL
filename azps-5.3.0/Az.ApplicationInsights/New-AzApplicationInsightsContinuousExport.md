---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApplicationInsights.dll-Help.xml
Module Name: Az.ApplicationInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.applicationinsights/new-azapplicationinsightscontinuousexport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/New-AzApplicationInsightsContinuousExport.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/New-AzApplicationInsightsContinuousExport.md
ms.openlocfilehash: 97994eb9898f5eca3e8f7f3015e2ce96845d5c24
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98381353"
---
# <span data-ttu-id="931e0-101">New-AzApplicationInsightsContinuousExport</span><span class="sxs-lookup"><span data-stu-id="931e0-101">New-AzApplicationInsightsContinuousExport</span></span>

## <span data-ttu-id="931e0-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="931e0-102">SYNOPSIS</span></span>
<span data-ttu-id="931e0-103">Tworzenie nowej konfiguracji ciągłego eksportu usługi Application Insights dla zasobu usługi Application Insights</span><span class="sxs-lookup"><span data-stu-id="931e0-103">Create a new application insights continuous export configuration for an application insights resource</span></span>

## <span data-ttu-id="931e0-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="931e0-104">SYNTAX</span></span>

### <span data-ttu-id="931e0-105">ComponentNameParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="931e0-105">ComponentNameParameterSet (Default)</span></span>
```
New-AzApplicationInsightsContinuousExport [-ResourceGroupName] <String> [-Name] <String>
 -DocumentType <String[]> -StorageAccountId <String> -StorageLocation <String> -StorageSASUri <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="931e0-106">ComponentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="931e0-106">ComponentObjectParameterSet</span></span>
```
New-AzApplicationInsightsContinuousExport [-ApplicationInsightsComponent] <PSApplicationInsightsComponent>
 -DocumentType <String[]> -StorageAccountId <String> -StorageLocation <String> -StorageSASUri <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="931e0-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="931e0-107">ResourceIdParameterSet</span></span>
```
New-AzApplicationInsightsContinuousExport [-ResourceId] <String> -DocumentType <String[]>
 -StorageAccountId <String> -StorageLocation <String> -StorageSASUri <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="931e0-108">Opis</span><span class="sxs-lookup"><span data-stu-id="931e0-108">DESCRIPTION</span></span>
<span data-ttu-id="931e0-109">Tworzenie nowej konfiguracji ciągłego eksportu usługi Application Insights dla zasobu usługi Application Insights</span><span class="sxs-lookup"><span data-stu-id="931e0-109">Create a new application insights continuous export configuration for an application insights resource</span></span>

## <span data-ttu-id="931e0-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="931e0-110">EXAMPLES</span></span>

### <span data-ttu-id="931e0-111">Przykład 1 Tworzenie nowej ciągłej konfiguracji eksportu dla zasobu usługi Application Insights</span><span class="sxs-lookup"><span data-stu-id="931e0-111">Example 1 Create a new continuous export configuration for an application insights resource</span></span>
```
PS C:\> $sastoken = New-AzStorageContainerSASToken -Name testcontainer -Context $context -ExpiryTime (Get-Date).AddYears(50) -Permission w
PS C:\> $sasuri = "https://teststorageaccount.blob.core.windows.net/testcontainer" + $sastoken
PS C:\> New-AzApplicationInsightsContinuousExport -ResourceGroupName "testgroup" -Name "test"
 -DocumentType "Request","Trace", "Custom Event" -StorageAccountId "/subscriptions/50359d91-7b9d-4823-85af-eb298a61ba96/resourceGroups/testgroup/providers/Microsoft.Storage/storageAccounts/teststorageaccount" -StorageLocation sourcecentralus
 -StorageSASUri $sasuri

ExportId                         : jlTFEiBg1rkDXOCIeJQ2mB2TxZg=
StorageName                      : teststorageaccount
ContainerName                    : testcontainer
DocumentTypes                    : Request, Custom Event, Trace
DestinationStorageSubscriptionId : 50359d91-7b9d-4823-85af-eb298a61ba96
DestinationStorageLocationId     : sourcecentralus
DestinationStorageAccountId      : /subscriptions/50359d91-7b9d-4823-85af-eb298a61ba96/resourceGroups/testgroup/providers/Microsoft.Storage/storageAccounts/teststorageaccount
IsEnabled                        : True
ExportStatus                     : Preparing
LastSuccessTime                  :
```

<span data-ttu-id="931e0-112">Utwórz nową, ciągłą konfigurację eksportowania w usłudze Application Insights, aby wyeksportować typy dokumentów "Request" i "Trace" do magazynu zawierającego "testcontainer" na koncie magazynu "teststorageaccount" w grupie zasobów "Tester".</span><span class="sxs-lookup"><span data-stu-id="931e0-112">Create a new application insights continuous export configuration to export "Request" and "Trace" document types to storage contain "testcontainer" in storage account "teststorageaccount" in resource group "testgroup".</span></span> <span data-ttu-id="931e0-113">Token SAS musi być prawidłowy i mieć uprawnienie do zapisu w kontenerze, w przeciwnym razie Funkcja eksportu ciągłego nie będzie działać. Jeśli token SAS wygasł, Funkcja eksportu ciągłego przestanie działać.</span><span class="sxs-lookup"><span data-stu-id="931e0-113">The SAS token have to be valid and have write permission to the container, otherwise continuous export feature won't work.If SAS token expired, the continuous export feature will stop working.</span></span>

## <span data-ttu-id="931e0-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="931e0-114">PARAMETERS</span></span>

### <span data-ttu-id="931e0-115">-ApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="931e0-115">-ApplicationInsightsComponent</span></span>
<span data-ttu-id="931e0-116">Obiekt składnika Application Insights.</span><span class="sxs-lookup"><span data-stu-id="931e0-116">Application Insights Component Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApplicationInsights.Models.PSApplicationInsightsComponent
Parameter Sets: ComponentObjectParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="931e0-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="931e0-117">-DefaultProfile</span></span>
<span data-ttu-id="931e0-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="931e0-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="931e0-119">-DocumentType</span><span class="sxs-lookup"><span data-stu-id="931e0-119">-DocumentType</span></span>
<span data-ttu-id="931e0-120">Typy dokumentów, które muszą być eksportowane.</span><span class="sxs-lookup"><span data-stu-id="931e0-120">Document types that need exported.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:
Accepted values: Request, Exception, Custom Event, Trace, Metric, Page Load, Page View, Dependency, Availability, Performance Counter

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="931e0-121">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="931e0-121">-Name</span></span>
<span data-ttu-id="931e0-122">Nazwa składnika.</span><span class="sxs-lookup"><span data-stu-id="931e0-122">Component Name.</span></span>

```yaml
Type: System.String
Parameter Sets: ComponentNameParameterSet
Aliases: ApplicationInsightsComponentName, ComponentName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="931e0-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="931e0-123">-ResourceGroupName</span></span>
<span data-ttu-id="931e0-124">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="931e0-124">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: ComponentNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="931e0-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="931e0-125">-ResourceId</span></span>
<span data-ttu-id="931e0-126">Identyfikator zasobu składnika Application Insights.</span><span class="sxs-lookup"><span data-stu-id="931e0-126">Application Insights Component Resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="931e0-127">-StorageAccountId</span><span class="sxs-lookup"><span data-stu-id="931e0-127">-StorageAccountId</span></span>
<span data-ttu-id="931e0-128">Identyfikator konta magazynu docelowego.</span><span class="sxs-lookup"><span data-stu-id="931e0-128">Destination Storage Account Id.</span></span>

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

### <span data-ttu-id="931e0-129">-StorageLocation</span><span class="sxs-lookup"><span data-stu-id="931e0-129">-StorageLocation</span></span>
<span data-ttu-id="931e0-130">Identyfikator docelowej lokalizacji przechowywania.</span><span class="sxs-lookup"><span data-stu-id="931e0-130">Destination Storage Location Id.</span></span>

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

### <span data-ttu-id="931e0-131">-StorageSASUri</span><span class="sxs-lookup"><span data-stu-id="931e0-131">-StorageSASUri</span></span>
<span data-ttu-id="931e0-132">Identyfikator URI SAS magazynu docelowego.</span><span class="sxs-lookup"><span data-stu-id="931e0-132">Destination Storage SAS Uri.</span></span>

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

### <span data-ttu-id="931e0-133">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="931e0-133">-Confirm</span></span>
<span data-ttu-id="931e0-134">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="931e0-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="931e0-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="931e0-135">-WhatIf</span></span>
<span data-ttu-id="931e0-136">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="931e0-136">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="931e0-137">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="931e0-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="931e0-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="931e0-138">CommonParameters</span></span>
<span data-ttu-id="931e0-139">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="931e0-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="931e0-140">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="931e0-140">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="931e0-141">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="931e0-141">INPUTS</span></span>

### <span data-ttu-id="931e0-142">Microsoft. Azure. Commands. ApplicationInsights. models. PSApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="931e0-142">Microsoft.Azure.Commands.ApplicationInsights.Models.PSApplicationInsightsComponent</span></span>

### <span data-ttu-id="931e0-143">System. String</span><span class="sxs-lookup"><span data-stu-id="931e0-143">System.String</span></span>

## <span data-ttu-id="931e0-144">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="931e0-144">OUTPUTS</span></span>

### <span data-ttu-id="931e0-145">Microsoft. Azure. Commands. ApplicationInsights. models. PSExportConfiguration</span><span class="sxs-lookup"><span data-stu-id="931e0-145">Microsoft.Azure.Commands.ApplicationInsights.Models.PSExportConfiguration</span></span>

## <span data-ttu-id="931e0-146">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="931e0-146">NOTES</span></span>

## <span data-ttu-id="931e0-147">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="931e0-147">RELATED LINKS</span></span>
