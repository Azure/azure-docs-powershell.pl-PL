---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApplicationInsights.dll-Help.xml
Module Name: Az.ApplicationInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.applicationinsights/set-azapplicationinsightscontinuousexport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/Set-AzApplicationInsightsContinuousExport.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/Set-AzApplicationInsightsContinuousExport.md
ms.openlocfilehash: 3927997ddca6c58c4ac97a0234291cac08777c6a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93706857"
---
# <span data-ttu-id="3cf8e-101">Set-AzApplicationInsightsContinuousExport</span><span class="sxs-lookup"><span data-stu-id="3cf8e-101">Set-AzApplicationInsightsContinuousExport</span></span>

## <span data-ttu-id="3cf8e-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="3cf8e-102">SYNOPSIS</span></span>
<span data-ttu-id="3cf8e-103">Aktualizowanie ciągłej konfiguracji eksportu w zasobie Application Insights</span><span class="sxs-lookup"><span data-stu-id="3cf8e-103">Update a continuous export configuration in an application insights resource</span></span>

## <span data-ttu-id="3cf8e-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="3cf8e-104">SYNTAX</span></span>

### <span data-ttu-id="3cf8e-105">ComponentNameParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="3cf8e-105">ComponentNameParameterSet (Default)</span></span>
```
Set-AzApplicationInsightsContinuousExport [-ResourceGroupName] <String> [-Name] <String> -ExportId <String>
 -DocumentType <String[]> -StorageAccountId <String> -StorageLocation <String> -StorageSASUri <String>
 [-DisableConfiguration] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3cf8e-106">ComponentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="3cf8e-106">ComponentObjectParameterSet</span></span>
```
Set-AzApplicationInsightsContinuousExport [-ApplicationInsightsComponent] <PSApplicationInsightsComponent>
 -ExportId <String> -DocumentType <String[]> -StorageAccountId <String> -StorageLocation <String>
 -StorageSASUri <String> [-DisableConfiguration] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3cf8e-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="3cf8e-107">ResourceIdParameterSet</span></span>
```
Set-AzApplicationInsightsContinuousExport [-ResourceId] <String> -ExportId <String> -DocumentType <String[]>
 -StorageAccountId <String> -StorageLocation <String> -StorageSASUri <String> [-DisableConfiguration]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3cf8e-108">Opis</span><span class="sxs-lookup"><span data-stu-id="3cf8e-108">DESCRIPTION</span></span>
<span data-ttu-id="3cf8e-109">Aktualizowanie ciągłej konfiguracji eksportu w zasobie Application Insights</span><span class="sxs-lookup"><span data-stu-id="3cf8e-109">Update a continuous export configuration in an application insights resource</span></span>

## <span data-ttu-id="3cf8e-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="3cf8e-110">EXAMPLES</span></span>

### <span data-ttu-id="3cf8e-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="3cf8e-111">Example 1</span></span>
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

<span data-ttu-id="3cf8e-112">Aktualizuj ciągłą konfigurację eksportu "jlTFEiBg1rkDXOCIeJQ2mB2TxZg =" zasobu "test" w grupie zasób "Aby wyeksportować dokumenty" Request "i" Trace "do kontenera magazynu" testcontainer "w" teststorageaccount ". Token SAS musi być prawidłowy i mieć uprawnienie do zapisu w kontenerze, w przeciwnym razie Funkcja eksportu ciągłego nie będzie działać.</span><span class="sxs-lookup"><span data-stu-id="3cf8e-112">Update continuous export configuration "jlTFEiBg1rkDXOCIeJQ2mB2TxZg=" of resource "test" in resource group "testgroup" to export "Request" and "Trace" documents to storage container "testcontainer" in "teststorageaccount".The SAS token have to be valid and have write permission to the container, otherwise continuous export feature won't work.</span></span> <span data-ttu-id="3cf8e-113">Jeśli token SAS wygasł, Funkcja eksportu ciągłego przestanie działać.</span><span class="sxs-lookup"><span data-stu-id="3cf8e-113">If SAS token expired, the continuous export feature will stop working.</span></span>

## <span data-ttu-id="3cf8e-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="3cf8e-114">PARAMETERS</span></span>

### <span data-ttu-id="3cf8e-115">-ApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="3cf8e-115">-ApplicationInsightsComponent</span></span>
<span data-ttu-id="3cf8e-116">Obiekt składnika Application Insights.</span><span class="sxs-lookup"><span data-stu-id="3cf8e-116">Application Insights Component Object.</span></span>

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

### <span data-ttu-id="3cf8e-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3cf8e-117">-DefaultProfile</span></span>
<span data-ttu-id="3cf8e-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="3cf8e-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3cf8e-119">-DisableConfiguration</span><span class="sxs-lookup"><span data-stu-id="3cf8e-119">-DisableConfiguration</span></span>
<span data-ttu-id="3cf8e-120">Wyłącz eksport ciągły lub nie.</span><span class="sxs-lookup"><span data-stu-id="3cf8e-120">Disable continuous export or not.</span></span>

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

### <span data-ttu-id="3cf8e-121">-DocumentType</span><span class="sxs-lookup"><span data-stu-id="3cf8e-121">-DocumentType</span></span>
<span data-ttu-id="3cf8e-122">Typy dokumentów, które muszą być eksportowane.</span><span class="sxs-lookup"><span data-stu-id="3cf8e-122">Document types that need exported.</span></span>

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

### <span data-ttu-id="3cf8e-123">-ExportId</span><span class="sxs-lookup"><span data-stu-id="3cf8e-123">-ExportId</span></span>
<span data-ttu-id="3cf8e-124">Identyfikator eksportu w usłudze Application Insights.</span><span class="sxs-lookup"><span data-stu-id="3cf8e-124">Application Insights Continuous Export Id.</span></span>

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

### <span data-ttu-id="3cf8e-125">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="3cf8e-125">-Name</span></span>
<span data-ttu-id="3cf8e-126">Nazwa składnika Application Insights.</span><span class="sxs-lookup"><span data-stu-id="3cf8e-126">Application Insights Component Name.</span></span>

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

### <span data-ttu-id="3cf8e-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3cf8e-127">-ResourceGroupName</span></span>
<span data-ttu-id="3cf8e-128">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="3cf8e-128">Resource Group Name.</span></span>

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

### <span data-ttu-id="3cf8e-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="3cf8e-129">-ResourceId</span></span>
<span data-ttu-id="3cf8e-130">Identyfikator zasobu składnika Application Insights.</span><span class="sxs-lookup"><span data-stu-id="3cf8e-130">Application Insights Component Resource Id.</span></span>

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

### <span data-ttu-id="3cf8e-131">-StorageAccountId</span><span class="sxs-lookup"><span data-stu-id="3cf8e-131">-StorageAccountId</span></span>
<span data-ttu-id="3cf8e-132">Identyfikator konta magazynu docelowego.</span><span class="sxs-lookup"><span data-stu-id="3cf8e-132">Destination Storage Account Id.</span></span>

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

### <span data-ttu-id="3cf8e-133">-StorageLocation</span><span class="sxs-lookup"><span data-stu-id="3cf8e-133">-StorageLocation</span></span>
<span data-ttu-id="3cf8e-134">Identyfikator docelowej lokalizacji przechowywania.</span><span class="sxs-lookup"><span data-stu-id="3cf8e-134">Destination Storage Location Id.</span></span>

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

### <span data-ttu-id="3cf8e-135">-StorageSASUri</span><span class="sxs-lookup"><span data-stu-id="3cf8e-135">-StorageSASUri</span></span>
<span data-ttu-id="3cf8e-136">Identyfikator URI SAS magazynu docelowego.</span><span class="sxs-lookup"><span data-stu-id="3cf8e-136">Destination Storage SAS uri.</span></span>

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

### <span data-ttu-id="3cf8e-137">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="3cf8e-137">-Confirm</span></span>
<span data-ttu-id="3cf8e-138">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3cf8e-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3cf8e-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3cf8e-139">-WhatIf</span></span>
<span data-ttu-id="3cf8e-140">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3cf8e-140">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="3cf8e-141">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="3cf8e-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3cf8e-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3cf8e-142">CommonParameters</span></span>
<span data-ttu-id="3cf8e-143">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3cf8e-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3cf8e-144">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3cf8e-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3cf8e-145">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="3cf8e-145">INPUTS</span></span>

### <span data-ttu-id="3cf8e-146">Microsoft. Azure. Commands. ApplicationInsights. models. PSApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="3cf8e-146">Microsoft.Azure.Commands.ApplicationInsights.Models.PSApplicationInsightsComponent</span></span>

### <span data-ttu-id="3cf8e-147">System. String</span><span class="sxs-lookup"><span data-stu-id="3cf8e-147">System.String</span></span>

## <span data-ttu-id="3cf8e-148">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="3cf8e-148">OUTPUTS</span></span>

### <span data-ttu-id="3cf8e-149">Microsoft. Azure. Commands. ApplicationInsights. models. PSExportConfiguration</span><span class="sxs-lookup"><span data-stu-id="3cf8e-149">Microsoft.Azure.Commands.ApplicationInsights.Models.PSExportConfiguration</span></span>

## <span data-ttu-id="3cf8e-150">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="3cf8e-150">NOTES</span></span>

## <span data-ttu-id="3cf8e-151">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="3cf8e-151">RELATED LINKS</span></span>
