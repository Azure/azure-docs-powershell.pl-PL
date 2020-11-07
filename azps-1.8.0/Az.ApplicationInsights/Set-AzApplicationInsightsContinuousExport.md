---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApplicationInsights.dll-Help.xml
Module Name: Az.ApplicationInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.applicationinsights/set-azapplicationinsightscontinuousexport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/Set-AzApplicationInsightsContinuousExport.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/Set-AzApplicationInsightsContinuousExport.md
ms.openlocfilehash: 04976e85104c702bb129882e942864f9a5b201ae
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93710619"
---
# <span data-ttu-id="16efe-101">Set-AzApplicationInsightsContinuousExport</span><span class="sxs-lookup"><span data-stu-id="16efe-101">Set-AzApplicationInsightsContinuousExport</span></span>

## <span data-ttu-id="16efe-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="16efe-102">SYNOPSIS</span></span>
<span data-ttu-id="16efe-103">Aktualizowanie ciągłej konfiguracji eksportu w zasobie applciation Insights</span><span class="sxs-lookup"><span data-stu-id="16efe-103">Update a continuous export configuration in an applciation insights resource</span></span>

## <span data-ttu-id="16efe-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="16efe-104">SYNTAX</span></span>

### <span data-ttu-id="16efe-105">ComponentNameParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="16efe-105">ComponentNameParameterSet (Default)</span></span>
```
Set-AzApplicationInsightsContinuousExport [-ResourceGroupName] <String> [-Name] <String> -ExportId <String>
 -DocumentType <String[]> -StorageAccountId <String> -StorageLocation <String> -StorageSASUri <String>
 [-DisableConfiguration] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="16efe-106">ComponentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="16efe-106">ComponentObjectParameterSet</span></span>
```
Set-AzApplicationInsightsContinuousExport [-ApplicationInsightsComponent] <PSApplicationInsightsComponent>
 -ExportId <String> -DocumentType <String[]> -StorageAccountId <String> -StorageLocation <String>
 -StorageSASUri <String> [-DisableConfiguration] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="16efe-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="16efe-107">ResourceIdParameterSet</span></span>
```
Set-AzApplicationInsightsContinuousExport [-ResourceId] <String> -ExportId <String> -DocumentType <String[]>
 -StorageAccountId <String> -StorageLocation <String> -StorageSASUri <String> [-DisableConfiguration]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="16efe-108">Opis</span><span class="sxs-lookup"><span data-stu-id="16efe-108">DESCRIPTION</span></span>
<span data-ttu-id="16efe-109">Aktualizowanie ciągłej konfiguracji eksportu w zasobie applciation Insights</span><span class="sxs-lookup"><span data-stu-id="16efe-109">Update a continuous export configuration in an applciation insights resource</span></span>

## <span data-ttu-id="16efe-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="16efe-110">EXAMPLES</span></span>

### <span data-ttu-id="16efe-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="16efe-111">Example 1</span></span>
```
PS C:\> $sastoken = New-AzStorageContainerSASToken -Name testcontainer -Context $context -ExpiryTime (Get-Date).AddYears(50) -Permission w
PS C:\> $sasuri = "https://teststorageaccount.blob.core.windows.net/testcontainer" + $sastoken
PS C:\> Set-AzApplicationInsightsContinuousExport -ResourceGroupName "testgroup" -Name "test"
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

<span data-ttu-id="16efe-112">Aktualizuj ciągłą konfigurację eksportu "jlTFEiBg1rkDXOCIeJQ2mB2TxZg =" zasobu "test" w grupie zasób "Aby wyeksportować dokumenty" Request "i" Trace "do kontenera magazynu" testcontainer "w" teststorageaccount ". Token SAS musi być prawidłowy i mieć uprawnienie do zapisu w kontenerze, w przeciwnym razie ciągła Funkcja eksportowania nie będzie działać.</span><span class="sxs-lookup"><span data-stu-id="16efe-112">Update continuous export configuration "jlTFEiBg1rkDXOCIeJQ2mB2TxZg=" of resource "test" in resource group "testgroup" to export "Request" and "Trace" documents to storage container "testcontainer" in "teststorageaccount".The SAS token have to be valid and have write permission to the container, otherwise continous export feature won't work.</span></span> <span data-ttu-id="16efe-113">Jeśli token SAS wygasł, Funkcja eksportu ciągłego przestanie działać.</span><span class="sxs-lookup"><span data-stu-id="16efe-113">If SAS token expired, the continuous export feature will stop working.</span></span>

## <span data-ttu-id="16efe-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="16efe-114">PARAMETERS</span></span>

### <span data-ttu-id="16efe-115">-ApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="16efe-115">-ApplicationInsightsComponent</span></span>
<span data-ttu-id="16efe-116">Obiekt składnika Application Insights.</span><span class="sxs-lookup"><span data-stu-id="16efe-116">Application Insights Component Object.</span></span>

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

### <span data-ttu-id="16efe-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="16efe-117">-DefaultProfile</span></span>
<span data-ttu-id="16efe-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="16efe-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="16efe-119">-DisableConfiguration</span><span class="sxs-lookup"><span data-stu-id="16efe-119">-DisableConfiguration</span></span>
<span data-ttu-id="16efe-120">Wyłącz eksport ciągły lub nie.</span><span class="sxs-lookup"><span data-stu-id="16efe-120">Disable continuous export or not.</span></span>

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

### <span data-ttu-id="16efe-121">-DocumentType</span><span class="sxs-lookup"><span data-stu-id="16efe-121">-DocumentType</span></span>
<span data-ttu-id="16efe-122">Typy dokumentów, które muszą być eksportowane.</span><span class="sxs-lookup"><span data-stu-id="16efe-122">Document types that need exported.</span></span>

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

### <span data-ttu-id="16efe-123">-ExportId</span><span class="sxs-lookup"><span data-stu-id="16efe-123">-ExportId</span></span>
<span data-ttu-id="16efe-124">Identyfikator eksportu w usłudze Application Insights.</span><span class="sxs-lookup"><span data-stu-id="16efe-124">Application Insights Continuous Export Id.</span></span>

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

### <span data-ttu-id="16efe-125">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="16efe-125">-Name</span></span>
<span data-ttu-id="16efe-126">Nazwa składnika Application Insights.</span><span class="sxs-lookup"><span data-stu-id="16efe-126">Application Insights Component Name.</span></span>

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

### <span data-ttu-id="16efe-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="16efe-127">-ResourceGroupName</span></span>
<span data-ttu-id="16efe-128">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="16efe-128">Resource Group Name.</span></span>

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

### <span data-ttu-id="16efe-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="16efe-129">-ResourceId</span></span>
<span data-ttu-id="16efe-130">Identyfikator zasobu składnika Application Insights.</span><span class="sxs-lookup"><span data-stu-id="16efe-130">Application Insights Component Resource Id.</span></span>

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

### <span data-ttu-id="16efe-131">-StorageAccountId</span><span class="sxs-lookup"><span data-stu-id="16efe-131">-StorageAccountId</span></span>
<span data-ttu-id="16efe-132">Identyfikator konta magazynu docelowego.</span><span class="sxs-lookup"><span data-stu-id="16efe-132">Destination Storage Account Id.</span></span>

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

### <span data-ttu-id="16efe-133">-StorageLocation</span><span class="sxs-lookup"><span data-stu-id="16efe-133">-StorageLocation</span></span>
<span data-ttu-id="16efe-134">Identyfikator docelowej lokalizacji przechowywania.</span><span class="sxs-lookup"><span data-stu-id="16efe-134">Destination Storage Location Id.</span></span>

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

### <span data-ttu-id="16efe-135">-StorageSASUri</span><span class="sxs-lookup"><span data-stu-id="16efe-135">-StorageSASUri</span></span>
<span data-ttu-id="16efe-136">Identyfikator URI SAS magazynu docelowego.</span><span class="sxs-lookup"><span data-stu-id="16efe-136">Destination Storage SAS uri.</span></span>

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

### <span data-ttu-id="16efe-137">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="16efe-137">-Confirm</span></span>
<span data-ttu-id="16efe-138">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="16efe-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="16efe-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="16efe-139">-WhatIf</span></span>
<span data-ttu-id="16efe-140">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="16efe-140">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="16efe-141">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="16efe-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="16efe-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="16efe-142">CommonParameters</span></span>
<span data-ttu-id="16efe-143">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="16efe-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="16efe-144">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="16efe-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="16efe-145">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="16efe-145">INPUTS</span></span>

### <span data-ttu-id="16efe-146">Microsoft. Azure. Commands. ApplicationInsights. models. PSApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="16efe-146">Microsoft.Azure.Commands.ApplicationInsights.Models.PSApplicationInsightsComponent</span></span>

### <span data-ttu-id="16efe-147">System. String</span><span class="sxs-lookup"><span data-stu-id="16efe-147">System.String</span></span>

## <span data-ttu-id="16efe-148">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="16efe-148">OUTPUTS</span></span>

### <span data-ttu-id="16efe-149">Microsoft. Azure. Commands. ApplicationInsights. models. PSExportConfiguration</span><span class="sxs-lookup"><span data-stu-id="16efe-149">Microsoft.Azure.Commands.ApplicationInsights.Models.PSExportConfiguration</span></span>

## <span data-ttu-id="16efe-150">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="16efe-150">NOTES</span></span>

## <span data-ttu-id="16efe-151">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="16efe-151">RELATED LINKS</span></span>
