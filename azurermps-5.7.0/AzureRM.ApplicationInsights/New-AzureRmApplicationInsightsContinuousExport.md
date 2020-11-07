---
external help file: Microsoft.Azure.Commands.ApplicationInsights.dll-Help.xml
Module Name: AzureRM.ApplicationInsights
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.applicationinsights/new-azurermapplicationinsightscontinuousexport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApplicationInsights/Commands.ApplicationInsights/help/New-AzureRmApplicationInsightsContinuousExport.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApplicationInsights/Commands.ApplicationInsights/help/New-AzureRmApplicationInsightsContinuousExport.md
ms.openlocfilehash: 1e4dd5f65789751f9a28deb9e10c37221f45b97b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93718061"
---
# <span data-ttu-id="599d8-101">New-AzureRmApplicationInsightsContinuousExport</span><span class="sxs-lookup"><span data-stu-id="599d8-101">New-AzureRmApplicationInsightsContinuousExport</span></span>

## <span data-ttu-id="599d8-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="599d8-102">SYNOPSIS</span></span>
<span data-ttu-id="599d8-103">Tworzenie nowej konfiguracji ciągłego eksportu usługi Application Insights dla zasobu usługi Application Insights</span><span class="sxs-lookup"><span data-stu-id="599d8-103">Create a new application insights continuous export configuration for an application insights resource</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="599d8-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="599d8-104">SYNTAX</span></span>

### <span data-ttu-id="599d8-105">ComponentNameParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="599d8-105">ComponentNameParameterSet (Default)</span></span>
```
New-AzureRmApplicationInsightsContinuousExport [-ResourceGroupName] <String> [-Name] <String>
 -DocumentType <String[]> -StorageAccountId <String> -StorageLocation <String> -StorageSASUri <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="599d8-106">ComponentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="599d8-106">ComponentObjectParameterSet</span></span>
```
New-AzureRmApplicationInsightsContinuousExport [-ApplicationInsightsComponent] <PSApplicationInsightsComponent>
 -DocumentType <String[]> -StorageAccountId <String> -StorageLocation <String> -StorageSASUri <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="599d8-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="599d8-107">ResourceIdParameterSet</span></span>
```
New-AzureRmApplicationInsightsContinuousExport [-ResourceId] <String> -DocumentType <String[]>
 -StorageAccountId <String> -StorageLocation <String> -StorageSASUri <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="599d8-108">Opis</span><span class="sxs-lookup"><span data-stu-id="599d8-108">DESCRIPTION</span></span>
<span data-ttu-id="599d8-109">Tworzenie nowej konfiguracji ciągłego eksportu usługi Application Insights dla zasobu usługi Application Insights</span><span class="sxs-lookup"><span data-stu-id="599d8-109">Create a new application insights continuous export configuration for an application insights resource</span></span>

## <span data-ttu-id="599d8-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="599d8-110">EXAMPLES</span></span>

### <span data-ttu-id="599d8-111">Przykład 1 Tworzenie nowej ciągłej konfiguracji eksportu dla zasobu usługi Application Insights</span><span class="sxs-lookup"><span data-stu-id="599d8-111">Example 1 Create a new continuous export configuration for an application insights resource</span></span>
```
PS C:\> $sastoken = New-AzureStorageContainerSASToken -Name testcontainer -Context $context -ExpiryTime (Get-Date).AddYears(50) -Permission w
PS C:\> $sasuri = "https://teststorageaccount.blob.core.windows.net/testcontainer" + $sastoken
PS C:\> New-AzureRmApplicationInsightsContinuousExport -ResourceGroupName "testgroup" -Name "test"
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

<span data-ttu-id="599d8-112">Utwórz nową, ciągłą konfigurację eksportowania w usłudze Application Insights, aby wyeksportować typy dokumentów "Request" i "Trace" do magazynu zawierającego "testcontainer" na koncie magazynu "teststorageaccount" w grupie zasobów "Tester".</span><span class="sxs-lookup"><span data-stu-id="599d8-112">Create a new application insights continuous export configuration to export "Request" and "Trace" document types to storage contain "testcontainer" in storage account "teststorageaccount" in resource group "testgroup".</span></span> <span data-ttu-id="599d8-113">Token SAS musi być prawidłowy i mieć uprawnienie do zapisu w kontenerze, w przeciwnym razie ciągła Funkcja eksportowania nie będzie działać. Jeśli token SAS wygasł, Funkcja eksportu ciągłego przestanie działać.</span><span class="sxs-lookup"><span data-stu-id="599d8-113">The SAS token have to be valid and have write permission to the container, otherwise continous export feature won't work.If SAS token expired, the continuous export feature will stop working.</span></span>

## <span data-ttu-id="599d8-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="599d8-114">PARAMETERS</span></span>

### <span data-ttu-id="599d8-115">-ApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="599d8-115">-ApplicationInsightsComponent</span></span>
<span data-ttu-id="599d8-116">Obiekt składnika Application Insights.</span><span class="sxs-lookup"><span data-stu-id="599d8-116">Application Insights Component Object.</span></span>

```yaml
Type: PSApplicationInsightsComponent
Parameter Sets: ComponentObjectParameterSet
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="599d8-117">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="599d8-117">-Confirm</span></span>
<span data-ttu-id="599d8-118">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="599d8-118">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="599d8-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="599d8-119">-DefaultProfile</span></span>
<span data-ttu-id="599d8-120">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="599d8-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="599d8-121">-DocumentType</span><span class="sxs-lookup"><span data-stu-id="599d8-121">-DocumentType</span></span>
<span data-ttu-id="599d8-122">Typy dokumentów, które muszą być eksportowane.</span><span class="sxs-lookup"><span data-stu-id="599d8-122">Document types that need exported.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 
Accepted values: Request, Exception, Custom Event, Trace, Metric, Page Load, Page View, Dependency, Availability, Performance Counter

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="599d8-123">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="599d8-123">-Name</span></span>
<span data-ttu-id="599d8-124">Nazwa składnika.</span><span class="sxs-lookup"><span data-stu-id="599d8-124">Component Name.</span></span>

```yaml
Type: String
Parameter Sets: ComponentNameParameterSet
Aliases: ApplicationInsightsComponentName, ComponentName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="599d8-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="599d8-125">-ResourceGroupName</span></span>
<span data-ttu-id="599d8-126">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="599d8-126">Resource Group Name.</span></span>

```yaml
Type: String
Parameter Sets: ComponentNameParameterSet
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="599d8-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="599d8-127">-ResourceId</span></span>
<span data-ttu-id="599d8-128">Identyfikator zasobu składnika Application Insights.</span><span class="sxs-lookup"><span data-stu-id="599d8-128">Application Insights Component Resource Id.</span></span>

```yaml
Type: String
Parameter Sets: ResourceIdParameterSet
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="599d8-129">-StorageAccountId</span><span class="sxs-lookup"><span data-stu-id="599d8-129">-StorageAccountId</span></span>
<span data-ttu-id="599d8-130">Identyfikator konta magazynu docelowego.</span><span class="sxs-lookup"><span data-stu-id="599d8-130">Destination Storage Account Id.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="599d8-131">-StorageLocation</span><span class="sxs-lookup"><span data-stu-id="599d8-131">-StorageLocation</span></span>
<span data-ttu-id="599d8-132">Identyfikator docelowej lokalizacji przechowywania.</span><span class="sxs-lookup"><span data-stu-id="599d8-132">Destination Storage Location Id.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="599d8-133">-StorageSASUri</span><span class="sxs-lookup"><span data-stu-id="599d8-133">-StorageSASUri</span></span>
<span data-ttu-id="599d8-134">Identyfikator URI SAS magazynu docelowego.</span><span class="sxs-lookup"><span data-stu-id="599d8-134">Destination Storage SAS Uri.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="599d8-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="599d8-135">-WhatIf</span></span>
<span data-ttu-id="599d8-136">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="599d8-136">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="599d8-137">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="599d8-137">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="599d8-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="599d8-138">CommonParameters</span></span>
<span data-ttu-id="599d8-139">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="599d8-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="599d8-140">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="599d8-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="599d8-141">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="599d8-141">INPUTS</span></span>

### <span data-ttu-id="599d8-142">System. String</span><span class="sxs-lookup"><span data-stu-id="599d8-142">System.String</span></span>
<span data-ttu-id="599d8-143">System. String []</span><span class="sxs-lookup"><span data-stu-id="599d8-143">System.String[]</span></span>

## <span data-ttu-id="599d8-144">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="599d8-144">OUTPUTS</span></span>

### <span data-ttu-id="599d8-145">Microsoft. Azure. Commands. ApplicationInsights. models. PSExportConfiguration</span><span class="sxs-lookup"><span data-stu-id="599d8-145">Microsoft.Azure.Commands.ApplicationInsights.Models.PSExportConfiguration</span></span>

## <span data-ttu-id="599d8-146">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="599d8-146">NOTES</span></span>

## <span data-ttu-id="599d8-147">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="599d8-147">RELATED LINKS</span></span>

