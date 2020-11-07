---
external help file: Microsoft.Azure.Commands.ApplicationInsights.dll-Help.xml
Module Name: AzureRM.ApplicationInsights
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.applicationinsights/set-azurermapplicationinsightscontinuousexport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApplicationInsights/Commands.ApplicationInsights/help/Set-AzureRmApplicationInsightsContinuousExport.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApplicationInsights/Commands.ApplicationInsights/help/Set-AzureRmApplicationInsightsContinuousExport.md
ms.openlocfilehash: 996dc0ee168b11ecf3610b0d977854e32dd769bb
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93716797"
---
# <span data-ttu-id="e14ef-101">Set-AzureRmApplicationInsightsContinuousExport</span><span class="sxs-lookup"><span data-stu-id="e14ef-101">Set-AzureRmApplicationInsightsContinuousExport</span></span>

## <span data-ttu-id="e14ef-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="e14ef-102">SYNOPSIS</span></span>
<span data-ttu-id="e14ef-103">Aktualizowanie ciągłej konfiguracji eksportu w zasobie applciation Insights</span><span class="sxs-lookup"><span data-stu-id="e14ef-103">Update a continuous export configuration in an applciation insights resource</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e14ef-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="e14ef-104">SYNTAX</span></span>

### <span data-ttu-id="e14ef-105">ComponentNameParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="e14ef-105">ComponentNameParameterSet (Default)</span></span>
```
Set-AzureRmApplicationInsightsContinuousExport [-ResourceGroupName] <String> [-Name] <String>
 -ExportId <String> -DocumentType <String[]> -StorageAccountId <String> -StorageLocation <String>
 -StorageSASUri <String> [-DisableConfiguration] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e14ef-106">ComponentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="e14ef-106">ComponentObjectParameterSet</span></span>
```
Set-AzureRmApplicationInsightsContinuousExport [-ApplicationInsightsComponent] <PSApplicationInsightsComponent>
 -ExportId <String> -DocumentType <String[]> -StorageAccountId <String> -StorageLocation <String>
 -StorageSASUri <String> [-DisableConfiguration] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e14ef-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="e14ef-107">ResourceIdParameterSet</span></span>
```
Set-AzureRmApplicationInsightsContinuousExport [-ResourceId] <String> -ExportId <String>
 -DocumentType <String[]> -StorageAccountId <String> -StorageLocation <String> -StorageSASUri <String>
 [-DisableConfiguration] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e14ef-108">Opis</span><span class="sxs-lookup"><span data-stu-id="e14ef-108">DESCRIPTION</span></span>
<span data-ttu-id="e14ef-109">Aktualizowanie ciągłej konfiguracji eksportu w zasobie applciation Insights</span><span class="sxs-lookup"><span data-stu-id="e14ef-109">Update a continuous export configuration in an applciation insights resource</span></span>

## <span data-ttu-id="e14ef-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="e14ef-110">EXAMPLES</span></span>

### <span data-ttu-id="e14ef-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="e14ef-111">Example 1</span></span>
```
PS C:\> $sastoken = New-AzureStorageContainerSASToken -Name testcontainer -Context $context -ExpiryTime (Get-Date).AddYears(50) -Permission w
PS C:\> $sasuri = "https://teststorageaccount.blob.core.windows.net/testcontainer" + $sastoken
PS C:\> Set-AzureRmApplicationInsightsContinuousExport -ResourceGroupName "testgroup" -Name "test"
 -DocumentTypes "Request","Trace" -ExportId "jlTFEiBg1rkDXOCIeJQ2mB2TxZg=" -DestinationStorageAccountId "/subscriptions/50359d91-7b9d-4823-85af-eb298a61ba96/resourceGroups/testgroup/providers/Microsoft.Storage/storageAccounts/teststorageaccount" -DestinationStorageLocationId sourcecentralus
 -DestinationStorageSASUri $sasuri

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

<span data-ttu-id="e14ef-112">Aktualizuj ciągłą konfigurację eksportu "jlTFEiBg1rkDXOCIeJQ2mB2TxZg =" zasobu "test" w grupie zasób "Aby wyeksportować dokumenty" Request "i" Trace "do kontenera magazynu" testcontainer "w" teststorageaccount ". Token SAS musi być prawidłowy i mieć uprawnienie do zapisu w kontenerze, w przeciwnym razie ciągła Funkcja eksportowania nie będzie działać.</span><span class="sxs-lookup"><span data-stu-id="e14ef-112">Update continuous export configuration "jlTFEiBg1rkDXOCIeJQ2mB2TxZg=" of resource "test" in resource group "testgroup" to export "Request" and "Trace" documents to storage container "testcontainer" in "teststorageaccount".The SAS token have to be valid and have write permission to the container, otherwise continous export feature won't work.</span></span> <span data-ttu-id="e14ef-113">Jeśli token SAS wygasł, Funkcja eksportu ciągłego przestanie działać.</span><span class="sxs-lookup"><span data-stu-id="e14ef-113">If SAS token expired, the continuous export feature will stop working.</span></span>

## <span data-ttu-id="e14ef-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="e14ef-114">PARAMETERS</span></span>

### <span data-ttu-id="e14ef-115">-ApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="e14ef-115">-ApplicationInsightsComponent</span></span>
<span data-ttu-id="e14ef-116">Obiekt składnika Application Insights.</span><span class="sxs-lookup"><span data-stu-id="e14ef-116">Application Insights Component Object.</span></span>

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

### <span data-ttu-id="e14ef-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e14ef-117">-DefaultProfile</span></span>
<span data-ttu-id="e14ef-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="e14ef-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e14ef-119">-DisableConfiguration</span><span class="sxs-lookup"><span data-stu-id="e14ef-119">-DisableConfiguration</span></span>
<span data-ttu-id="e14ef-120">Wyłącz eksport ciągły lub nie.</span><span class="sxs-lookup"><span data-stu-id="e14ef-120">Disable continuous export or not.</span></span>

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

### <span data-ttu-id="e14ef-121">-DocumentType</span><span class="sxs-lookup"><span data-stu-id="e14ef-121">-DocumentType</span></span>
<span data-ttu-id="e14ef-122">Typy dokumentów, które muszą być eksportowane.</span><span class="sxs-lookup"><span data-stu-id="e14ef-122">Document types that need exported.</span></span>

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

### <span data-ttu-id="e14ef-123">-ExportId</span><span class="sxs-lookup"><span data-stu-id="e14ef-123">-ExportId</span></span>
<span data-ttu-id="e14ef-124">Identyfikator eksportu w usłudze Application Insights.</span><span class="sxs-lookup"><span data-stu-id="e14ef-124">Application Insights Continuous Export Id.</span></span>

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

### <span data-ttu-id="e14ef-125">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="e14ef-125">-Name</span></span>
<span data-ttu-id="e14ef-126">Nazwa składnika Application Insights.</span><span class="sxs-lookup"><span data-stu-id="e14ef-126">Application Insights Component Name.</span></span>

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

### <span data-ttu-id="e14ef-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e14ef-127">-ResourceGroupName</span></span>
<span data-ttu-id="e14ef-128">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="e14ef-128">Resource Group Name.</span></span>

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

### <span data-ttu-id="e14ef-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e14ef-129">-ResourceId</span></span>
<span data-ttu-id="e14ef-130">Identyfikator zasobu składnika Application Insights.</span><span class="sxs-lookup"><span data-stu-id="e14ef-130">Application Insights Component Resource Id.</span></span>

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

### <span data-ttu-id="e14ef-131">-StorageAccountId</span><span class="sxs-lookup"><span data-stu-id="e14ef-131">-StorageAccountId</span></span>
<span data-ttu-id="e14ef-132">Identyfikator konta magazynu docelowego.</span><span class="sxs-lookup"><span data-stu-id="e14ef-132">Destination Storage Account Id.</span></span>

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

### <span data-ttu-id="e14ef-133">-StorageLocation</span><span class="sxs-lookup"><span data-stu-id="e14ef-133">-StorageLocation</span></span>
<span data-ttu-id="e14ef-134">Identyfikator docelowej lokalizacji przechowywania.</span><span class="sxs-lookup"><span data-stu-id="e14ef-134">Destination Storage Location Id.</span></span>

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

### <span data-ttu-id="e14ef-135">-StorageSASUri</span><span class="sxs-lookup"><span data-stu-id="e14ef-135">-StorageSASUri</span></span>
<span data-ttu-id="e14ef-136">Identyfikator URI SAS magazynu docelowego.</span><span class="sxs-lookup"><span data-stu-id="e14ef-136">Destination Storage SAS uri.</span></span>

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

### <span data-ttu-id="e14ef-137">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="e14ef-137">-Confirm</span></span>
<span data-ttu-id="e14ef-138">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e14ef-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e14ef-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e14ef-139">-WhatIf</span></span>
<span data-ttu-id="e14ef-140">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e14ef-140">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="e14ef-141">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="e14ef-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e14ef-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e14ef-142">CommonParameters</span></span>
<span data-ttu-id="e14ef-143">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e14ef-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e14ef-144">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e14ef-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e14ef-145">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e14ef-145">INPUTS</span></span>

### <span data-ttu-id="e14ef-146">Microsoft. Azure. Commands. ApplicationInsights. models. PSApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="e14ef-146">Microsoft.Azure.Commands.ApplicationInsights.Models.PSApplicationInsightsComponent</span></span>
<span data-ttu-id="e14ef-147">Parametry: ApplicationInsightsComponent (ByValue)</span><span class="sxs-lookup"><span data-stu-id="e14ef-147">Parameters: ApplicationInsightsComponent (ByValue)</span></span>

### <span data-ttu-id="e14ef-148">System. String</span><span class="sxs-lookup"><span data-stu-id="e14ef-148">System.String</span></span>

## <span data-ttu-id="e14ef-149">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="e14ef-149">OUTPUTS</span></span>

### <span data-ttu-id="e14ef-150">Microsoft. Azure. Commands. ApplicationInsights. models. PSExportConfiguration</span><span class="sxs-lookup"><span data-stu-id="e14ef-150">Microsoft.Azure.Commands.ApplicationInsights.Models.PSExportConfiguration</span></span>

## <span data-ttu-id="e14ef-151">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="e14ef-151">NOTES</span></span>

## <span data-ttu-id="e14ef-152">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="e14ef-152">RELATED LINKS</span></span>
