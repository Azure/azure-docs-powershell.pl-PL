---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApplicationInsights.dll-Help.xml
Module Name: Az.ApplicationInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.applicationinsights/get-azapplicationinsightscontinuousexport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/Get-AzApplicationInsightsContinuousExport.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/Get-AzApplicationInsightsContinuousExport.md
ms.openlocfilehash: e6e1e2319ade47557ddf07f34a9371a4bbd532b7
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93706869"
---
# <span data-ttu-id="30f7e-101">Get-AzApplicationInsightsContinuousExport</span><span class="sxs-lookup"><span data-stu-id="30f7e-101">Get-AzApplicationInsightsContinuousExport</span></span>

## <span data-ttu-id="30f7e-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="30f7e-102">SYNOPSIS</span></span>
<span data-ttu-id="30f7e-103">Uzyskiwanie ciągłej konfiguracji eksportu aplikacji Application Insights dla zasobu usługi Application Insights</span><span class="sxs-lookup"><span data-stu-id="30f7e-103">Get application insights continuous export configuration for an application insights resource</span></span>

## <span data-ttu-id="30f7e-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="30f7e-104">SYNTAX</span></span>

### <span data-ttu-id="30f7e-105">ComponentNameParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="30f7e-105">ComponentNameParameterSet (Default)</span></span>
```
Get-AzApplicationInsightsContinuousExport [-ResourceGroupName] <String> [-Name] <String> [[-ExportId] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="30f7e-106">ComponentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="30f7e-106">ComponentObjectParameterSet</span></span>
```
Get-AzApplicationInsightsContinuousExport [-ApplicationInsightsComponent] <PSApplicationInsightsComponent>
 [[-ExportId] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="30f7e-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="30f7e-107">ResourceIdParameterSet</span></span>
```
Get-AzApplicationInsightsContinuousExport [-ResourceId] <String> [[-ExportId] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="30f7e-108">Opis</span><span class="sxs-lookup"><span data-stu-id="30f7e-108">DESCRIPTION</span></span>
<span data-ttu-id="30f7e-109">Uzyskiwanie ciągłej konfiguracji eksportu aplikacji Application Insights dla zasobu usługi Application Insights</span><span class="sxs-lookup"><span data-stu-id="30f7e-109">Get application insights continuous export configuration for an application insights resource</span></span>

## <span data-ttu-id="30f7e-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="30f7e-110">EXAMPLES</span></span>

### <span data-ttu-id="30f7e-111">Przykład 1 pobieranie ciągłego eksportu dla zasobu usługi Application Insights</span><span class="sxs-lookup"><span data-stu-id="30f7e-111">Example 1 Get continuous export for an application insights resource</span></span>
```
PS C:\> Get-AzApplicationInsightsContinuousExport -ResourceGroupName "testgroup" -Name "test"

ExportId                     DocumentTypes                ExportStatus DestinationStorageAccountId
--------                     -------------                ------------ ---------------------------
ZJrfffySPdtG3ESn3iRxVIEFuNY= Request, Performance Counter Preparing    /subscriptions/{subid}...
```

<span data-ttu-id="30f7e-112">Uzyskiwanie ciągłych konfiguracji eksportu usługi Application Insights dla zasobu o nazwie "test" w grupie "testowanie"</span><span class="sxs-lookup"><span data-stu-id="30f7e-112">Get application insights continuous export configurations for resource named "test" in resource group "testgroup"</span></span>

### <span data-ttu-id="30f7e-113">Przykład 2 pobieranie ciągłego eksportu dla zasobu usługi Application Insights</span><span class="sxs-lookup"><span data-stu-id="30f7e-113">Example 2 Get continuous export for an application insights resource</span></span>
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

<span data-ttu-id="30f7e-114">Uzyskiwanie ciągłej konfiguracji eksportu usługi Application Insights z identyfikatorem eksportu "ZJrfffySPdtG3ESn3iRxVIEFuNY =" dla zasobu o nazwie "test" w grupie "testowanie"</span><span class="sxs-lookup"><span data-stu-id="30f7e-114">Get application insights continuous export configuration with export id "ZJrfffySPdtG3ESn3iRxVIEFuNY=" for resource named "test" in resource group "testgroup"</span></span>

## <span data-ttu-id="30f7e-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="30f7e-115">PARAMETERS</span></span>

### <span data-ttu-id="30f7e-116">-ApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="30f7e-116">-ApplicationInsightsComponent</span></span>
<span data-ttu-id="30f7e-117">Obiekt składnika Application Insights.</span><span class="sxs-lookup"><span data-stu-id="30f7e-117">Application Insights Component Object.</span></span>

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

### <span data-ttu-id="30f7e-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="30f7e-118">-DefaultProfile</span></span>
<span data-ttu-id="30f7e-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="30f7e-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="30f7e-120">-ExportId</span><span class="sxs-lookup"><span data-stu-id="30f7e-120">-ExportId</span></span>
<span data-ttu-id="30f7e-121">Identyfikator eksportu w usłudze Application Insights.</span><span class="sxs-lookup"><span data-stu-id="30f7e-121">Application Insights Continuous Export Id.</span></span>

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

### <span data-ttu-id="30f7e-122">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="30f7e-122">-Name</span></span>
<span data-ttu-id="30f7e-123">Nazwa składnika Application Insights.</span><span class="sxs-lookup"><span data-stu-id="30f7e-123">Application Insights Component Name.</span></span>

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

### <span data-ttu-id="30f7e-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="30f7e-124">-ResourceGroupName</span></span>
<span data-ttu-id="30f7e-125">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="30f7e-125">Resource Group Name.</span></span>

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

### <span data-ttu-id="30f7e-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="30f7e-126">-ResourceId</span></span>
<span data-ttu-id="30f7e-127">Identyfikator zasobu składnika Application Insights.</span><span class="sxs-lookup"><span data-stu-id="30f7e-127">Application Insights Component Resource Id.</span></span>

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

### <span data-ttu-id="30f7e-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="30f7e-128">CommonParameters</span></span>
<span data-ttu-id="30f7e-129">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="30f7e-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="30f7e-130">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="30f7e-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="30f7e-131">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="30f7e-131">INPUTS</span></span>

### <span data-ttu-id="30f7e-132">Microsoft. Azure. Commands. ApplicationInsights. models. PSApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="30f7e-132">Microsoft.Azure.Commands.ApplicationInsights.Models.PSApplicationInsightsComponent</span></span>

### <span data-ttu-id="30f7e-133">System. String</span><span class="sxs-lookup"><span data-stu-id="30f7e-133">System.String</span></span>

## <span data-ttu-id="30f7e-134">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="30f7e-134">OUTPUTS</span></span>

### <span data-ttu-id="30f7e-135">Microsoft. Azure. Commands. ApplicationInsights. models. PSExportConfiguration</span><span class="sxs-lookup"><span data-stu-id="30f7e-135">Microsoft.Azure.Commands.ApplicationInsights.Models.PSExportConfiguration</span></span>

## <span data-ttu-id="30f7e-136">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="30f7e-136">NOTES</span></span>

## <span data-ttu-id="30f7e-137">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="30f7e-137">RELATED LINKS</span></span>
