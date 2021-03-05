---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApplicationInsights.dll-Help.xml
Module Name: Az.ApplicationInsights
online version: https://docs.microsoft.com/powershell/module/az.applicationinsights/set-azapplicationinsightscontinuousexport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/Set-AzApplicationInsightsContinuousExport.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/Set-AzApplicationInsightsContinuousExport.md
ms.openlocfilehash: 144200f95ca7cff8b4fa541666912d62ba6bd0b6
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101966817"
---
# <span data-ttu-id="6da37-101">Set-AzApplicationInsightsContinuousExport</span><span class="sxs-lookup"><span data-stu-id="6da37-101">Set-AzApplicationInsightsContinuousExport</span></span>

## <span data-ttu-id="6da37-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6da37-102">SYNOPSIS</span></span>
<span data-ttu-id="6da37-103">Aktualizowanie konfiguracji ciągłego eksportu w zasobie szczegółowych informacji o aplikacjach</span><span class="sxs-lookup"><span data-stu-id="6da37-103">Update a continuous export configuration in an application insights resource</span></span>

## <span data-ttu-id="6da37-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="6da37-104">SYNTAX</span></span>

### <span data-ttu-id="6da37-105">ComponentNameParameterSet (Domyślne)</span><span class="sxs-lookup"><span data-stu-id="6da37-105">ComponentNameParameterSet (Default)</span></span>
```
Set-AzApplicationInsightsContinuousExport [-ResourceGroupName] <String> [-Name] <String> -ExportId <String>
 -DocumentType <String[]> -StorageAccountId <String> -StorageLocation <String> -StorageSASUri <String>
 [-DisableConfiguration] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6da37-106">ComponentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="6da37-106">ComponentObjectParameterSet</span></span>
```
Set-AzApplicationInsightsContinuousExport [-ApplicationInsightsComponent] <PSApplicationInsightsComponent>
 -ExportId <String> -DocumentType <String[]> -StorageAccountId <String> -StorageLocation <String>
 -StorageSASUri <String> [-DisableConfiguration] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6da37-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="6da37-107">ResourceIdParameterSet</span></span>
```
Set-AzApplicationInsightsContinuousExport [-ResourceId] <String> -ExportId <String> -DocumentType <String[]>
 -StorageAccountId <String> -StorageLocation <String> -StorageSASUri <String> [-DisableConfiguration]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6da37-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="6da37-108">DESCRIPTION</span></span>
<span data-ttu-id="6da37-109">Aktualizowanie konfiguracji ciągłego eksportu w zasobie szczegółowych informacji o aplikacjach</span><span class="sxs-lookup"><span data-stu-id="6da37-109">Update a continuous export configuration in an application insights resource</span></span>

## <span data-ttu-id="6da37-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="6da37-110">EXAMPLES</span></span>

### <span data-ttu-id="6da37-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="6da37-111">Example 1</span></span>
```
PS C:\> $sastoken = New-AzStorageContainerSASToken -Name testcontainer -Context $context -ExpiryTime (Get-Date).AddYears(50) -Permission w
PS C:\> $sasuri = "https://teststorageaccount.blob.core.windows.net/testcontainer" + $sastoken
PS C:\> Set-AzApplicationInsightsContinuousExport -ResourceGroupName "testgroup" -Name "test"
 -DocumentTypes "Request","Trace" -ExportId "jlTFEiBg1rkDXOCIeJQ2mB2TxZg=" -StorageAccountId "/subscriptions/50359d91-7b9d-4823-85af-eb298a61ba96/resourceGroups/testgroup/providers/Microsoft.Storage/storageAccounts/teststorageaccount" -StorageLocation sourcecentralus
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

<span data-ttu-id="6da37-112">Zaktualizuj konfigurację eksportu ciągłego "jlTFEiBg1rkDXOCIeJQ2mB2TxZg=" zasobu "test" w grupie zasobów "grupa testowa", aby wyeksportować dokumenty "Żądanie" i "Śledzenie" do kontenera magazynu "testcontainer" w "testtorageaccount". Token SAS musi być prawidłowy i mieć uprawnienie do zapisu w kontenerze, w przeciwnym razie funkcja eksportu ciągłego nie będzie działać.</span><span class="sxs-lookup"><span data-stu-id="6da37-112">Update continuous export configuration "jlTFEiBg1rkDXOCIeJQ2mB2TxZg=" of resource "test" in resource group "testgroup" to export "Request" and "Trace" documents to storage container "testcontainer" in "teststorageaccount".The SAS token have to be valid and have write permission to the container, otherwise continuous export feature won't work.</span></span> <span data-ttu-id="6da37-113">Jeśli token SAS wygasł, funkcja eksportu ciągłego przestanie działać.</span><span class="sxs-lookup"><span data-stu-id="6da37-113">If SAS token expired, the continuous export feature will stop working.</span></span>

## <span data-ttu-id="6da37-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6da37-114">PARAMETERS</span></span>

### <span data-ttu-id="6da37-115">-ApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="6da37-115">-ApplicationInsightsComponent</span></span>
<span data-ttu-id="6da37-116">Obiekt składnika Szczegółowe informacje o aplikacji.</span><span class="sxs-lookup"><span data-stu-id="6da37-116">Application Insights Component Object.</span></span>

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

### <span data-ttu-id="6da37-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6da37-117">-DefaultProfile</span></span>
<span data-ttu-id="6da37-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="6da37-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6da37-119">-DisableConfiguration</span><span class="sxs-lookup"><span data-stu-id="6da37-119">-DisableConfiguration</span></span>
<span data-ttu-id="6da37-120">Wyłącz ciągły eksport.</span><span class="sxs-lookup"><span data-stu-id="6da37-120">Disable continuous export or not.</span></span>

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

### <span data-ttu-id="6da37-121">-DocumentType</span><span class="sxs-lookup"><span data-stu-id="6da37-121">-DocumentType</span></span>
<span data-ttu-id="6da37-122">Typy dokumentów, które wymagają wyeksportowania.</span><span class="sxs-lookup"><span data-stu-id="6da37-122">Document types that need exported.</span></span>

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

### <span data-ttu-id="6da37-123">- ExportId</span><span class="sxs-lookup"><span data-stu-id="6da37-123">-ExportId</span></span>
<span data-ttu-id="6da37-124">Ciągły identyfikator eksportu aplikacji Insights.</span><span class="sxs-lookup"><span data-stu-id="6da37-124">Application Insights Continuous Export Id.</span></span>

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

### <span data-ttu-id="6da37-125">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="6da37-125">-Name</span></span>
<span data-ttu-id="6da37-126">Nazwa składnika szczegółowych informacji aplikacji.</span><span class="sxs-lookup"><span data-stu-id="6da37-126">Application Insights Component Name.</span></span>

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

### <span data-ttu-id="6da37-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6da37-127">-ResourceGroupName</span></span>
<span data-ttu-id="6da37-128">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="6da37-128">Resource Group Name.</span></span>

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

### <span data-ttu-id="6da37-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="6da37-129">-ResourceId</span></span>
<span data-ttu-id="6da37-130">Identyfikator składnika szczegółowych informacji aplikacji.</span><span class="sxs-lookup"><span data-stu-id="6da37-130">Application Insights Component Resource Id.</span></span>

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

### <span data-ttu-id="6da37-131">- StorageAccountId</span><span class="sxs-lookup"><span data-stu-id="6da37-131">-StorageAccountId</span></span>
<span data-ttu-id="6da37-132">Identyfikator konta magazynu docelowego.</span><span class="sxs-lookup"><span data-stu-id="6da37-132">Destination Storage Account Id.</span></span>

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

### <span data-ttu-id="6da37-133">-StorageLocation</span><span class="sxs-lookup"><span data-stu-id="6da37-133">-StorageLocation</span></span>
<span data-ttu-id="6da37-134">Identyfikator lokalizacji przechowywania docelowego.</span><span class="sxs-lookup"><span data-stu-id="6da37-134">Destination Storage Location Id.</span></span>

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

### <span data-ttu-id="6da37-135">-StorageSASUri</span><span class="sxs-lookup"><span data-stu-id="6da37-135">-StorageSASUri</span></span>
<span data-ttu-id="6da37-136">Destination Storage SAS uri.</span><span class="sxs-lookup"><span data-stu-id="6da37-136">Destination Storage SAS uri.</span></span>

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

### <span data-ttu-id="6da37-137">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="6da37-137">-Confirm</span></span>
<span data-ttu-id="6da37-138">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="6da37-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6da37-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6da37-139">-WhatIf</span></span>
<span data-ttu-id="6da37-140">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6da37-140">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="6da37-141">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="6da37-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6da37-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6da37-142">CommonParameters</span></span>
<span data-ttu-id="6da37-143">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6da37-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6da37-144">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6da37-144">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6da37-145">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="6da37-145">INPUTS</span></span>

### <span data-ttu-id="6da37-146">Microsoft.Azure.Commands.ApplicationInsights.Models.PSApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="6da37-146">Microsoft.Azure.Commands.ApplicationInsights.Models.PSApplicationInsightsComponent</span></span>

### <span data-ttu-id="6da37-147">System.String</span><span class="sxs-lookup"><span data-stu-id="6da37-147">System.String</span></span>

## <span data-ttu-id="6da37-148">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="6da37-148">OUTPUTS</span></span>

### <span data-ttu-id="6da37-149">Microsoft.Azure.Commands.ApplicationInsights.Models.PSExportConfiguration</span><span class="sxs-lookup"><span data-stu-id="6da37-149">Microsoft.Azure.Commands.ApplicationInsights.Models.PSExportConfiguration</span></span>

## <span data-ttu-id="6da37-150">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="6da37-150">NOTES</span></span>

## <span data-ttu-id="6da37-151">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="6da37-151">RELATED LINKS</span></span>
