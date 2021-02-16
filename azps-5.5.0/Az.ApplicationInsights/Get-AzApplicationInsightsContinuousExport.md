---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApplicationInsights.dll-Help.xml
Module Name: Az.ApplicationInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.applicationinsights/get-azapplicationinsightscontinuousexport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/Get-AzApplicationInsightsContinuousExport.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/Get-AzApplicationInsightsContinuousExport.md
ms.openlocfilehash: d5711e6bca9b0579b456e4d2b0c5f915b4ad6fe0
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100195298"
---
# <span data-ttu-id="65e18-101">Get-AzApplicationInsightsContinuousExport</span><span class="sxs-lookup"><span data-stu-id="65e18-101">Get-AzApplicationInsightsContinuousExport</span></span>

## <span data-ttu-id="65e18-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="65e18-102">SYNOPSIS</span></span>
<span data-ttu-id="65e18-103">Uzyskiwanie szczegółowych informacji o aplikacji w ciągłej konfiguracji eksportu dla zasobu szczegółowych informacji o aplikacjach</span><span class="sxs-lookup"><span data-stu-id="65e18-103">Get application insights continuous export configuration for an application insights resource</span></span>

## <span data-ttu-id="65e18-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="65e18-104">SYNTAX</span></span>

### <span data-ttu-id="65e18-105">ComponentNameParameterSet (Domyślne)</span><span class="sxs-lookup"><span data-stu-id="65e18-105">ComponentNameParameterSet (Default)</span></span>
```
Get-AzApplicationInsightsContinuousExport [-ResourceGroupName] <String> [-Name] <String> [[-ExportId] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="65e18-106">ComponentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="65e18-106">ComponentObjectParameterSet</span></span>
```
Get-AzApplicationInsightsContinuousExport [-ApplicationInsightsComponent] <PSApplicationInsightsComponent>
 [[-ExportId] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="65e18-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="65e18-107">ResourceIdParameterSet</span></span>
```
Get-AzApplicationInsightsContinuousExport [-ResourceId] <String> [[-ExportId] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="65e18-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="65e18-108">DESCRIPTION</span></span>
<span data-ttu-id="65e18-109">Uzyskiwanie szczegółowych informacji o aplikacji w ciągłej konfiguracji eksportu dla zasobu szczegółowych informacji o aplikacjach</span><span class="sxs-lookup"><span data-stu-id="65e18-109">Get application insights continuous export configuration for an application insights resource</span></span>

## <span data-ttu-id="65e18-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="65e18-110">EXAMPLES</span></span>

### <span data-ttu-id="65e18-111">Przykład 1 Uzyskiwanie ciągłego eksportu dla zasobu szczegółowych informacji o aplikacjach</span><span class="sxs-lookup"><span data-stu-id="65e18-111">Example 1 Get continuous export for an application insights resource</span></span>
```
PS C:\> Get-AzApplicationInsightsContinuousExport -ResourceGroupName "testgroup" -Name "test"

ExportId                     DocumentTypes                ExportStatus DestinationStorageAccountId
--------                     -------------                ------------ ---------------------------
ZJrfffySPdtG3ESn3iRxVIEFuNY= Request, Performance Counter Preparing    /subscriptions/{subid}...
```

<span data-ttu-id="65e18-112">Uzyskiwanie szczegółowych informacji o aplikacjach w ciągłych konfiguracjach eksportowania dla zasobu o nazwie "test" w grupie zasobów "grupa testowa"</span><span class="sxs-lookup"><span data-stu-id="65e18-112">Get application insights continuous export configurations for resource named "test" in resource group "testgroup"</span></span>

### <span data-ttu-id="65e18-113">Przykład 2 Uzyskiwanie ciągłego eksportu dla zasobu szczegółowych informacji o aplikacjach</span><span class="sxs-lookup"><span data-stu-id="65e18-113">Example 2 Get continuous export for an application insights resource</span></span>
```
PS C:\> Get-AzApplicationInsightsContinuousExport -ResourceGroupName "testgroup" -Name "test" -ExportId "ZJrfffySPdtG3ESn3iRxVIEFuNY="

ExportId                         : ZJrfffySPdtG3ESn3iRxVIEFuNY=
StorageName                      : targetaccount
ContainerName                    : continuousexport
DocumentTypes                    : Request, Performance Counter
DestinationStorageSubscriptionId : {subid}
DestinationStorageLocationId     : eastus
DestinationStorageAccountId      : /subscriptions/{subid}/resourceGroups/targetstorage/providers/Microsoft.Storage/storageAccounts/targetaccount
IsEnabled                        : True
ExportStatus                     : Preparing
LastSuccessTime                  :
```

<span data-ttu-id="65e18-114">Uzyskiwanie szczegółowych informacji o aplikacji o ciągłej konfiguracji eksportu z identyfikatorem eksportu "ZJrfffySPdtG3ESn3iRxPIAFuNY=" dla zasobu o nazwie "test" w grupie zasobów "grupa testowa"</span><span class="sxs-lookup"><span data-stu-id="65e18-114">Get application insights continuous export configuration with export id "ZJrfffySPdtG3ESn3iRxVIEFuNY=" for resource named "test" in resource group "testgroup"</span></span>

## <span data-ttu-id="65e18-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="65e18-115">PARAMETERS</span></span>

### <span data-ttu-id="65e18-116">-ApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="65e18-116">-ApplicationInsightsComponent</span></span>
<span data-ttu-id="65e18-117">Obiekt składnika Szczegółowe informacje o aplikacji.</span><span class="sxs-lookup"><span data-stu-id="65e18-117">Application Insights Component Object.</span></span>

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

### <span data-ttu-id="65e18-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="65e18-118">-DefaultProfile</span></span>
<span data-ttu-id="65e18-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="65e18-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="65e18-120">- ExportId</span><span class="sxs-lookup"><span data-stu-id="65e18-120">-ExportId</span></span>
<span data-ttu-id="65e18-121">Ciągły identyfikator eksportu aplikacji Insights.</span><span class="sxs-lookup"><span data-stu-id="65e18-121">Application Insights Continuous Export Id.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="65e18-122">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="65e18-122">-Name</span></span>
<span data-ttu-id="65e18-123">Nazwa składnika szczegółowych informacji aplikacji.</span><span class="sxs-lookup"><span data-stu-id="65e18-123">Application Insights Component Name.</span></span>

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

### <span data-ttu-id="65e18-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="65e18-124">-ResourceGroupName</span></span>
<span data-ttu-id="65e18-125">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="65e18-125">Resource Group Name.</span></span>

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

### <span data-ttu-id="65e18-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="65e18-126">-ResourceId</span></span>
<span data-ttu-id="65e18-127">Identyfikator składnika szczegółowych informacji aplikacji.</span><span class="sxs-lookup"><span data-stu-id="65e18-127">Application Insights Component Resource Id.</span></span>

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

### <span data-ttu-id="65e18-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="65e18-128">CommonParameters</span></span>
<span data-ttu-id="65e18-129">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="65e18-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="65e18-130">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="65e18-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="65e18-131">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="65e18-131">INPUTS</span></span>

### <span data-ttu-id="65e18-132">Microsoft.Azure.Commands.ApplicationInsights.Models.PSApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="65e18-132">Microsoft.Azure.Commands.ApplicationInsights.Models.PSApplicationInsightsComponent</span></span>

### <span data-ttu-id="65e18-133">System.String</span><span class="sxs-lookup"><span data-stu-id="65e18-133">System.String</span></span>

## <span data-ttu-id="65e18-134">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="65e18-134">OUTPUTS</span></span>

### <span data-ttu-id="65e18-135">Microsoft.Azure.Commands.ApplicationInsights.Models.PSExportConfiguration</span><span class="sxs-lookup"><span data-stu-id="65e18-135">Microsoft.Azure.Commands.ApplicationInsights.Models.PSExportConfiguration</span></span>

## <span data-ttu-id="65e18-136">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="65e18-136">NOTES</span></span>

## <span data-ttu-id="65e18-137">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="65e18-137">RELATED LINKS</span></span>
