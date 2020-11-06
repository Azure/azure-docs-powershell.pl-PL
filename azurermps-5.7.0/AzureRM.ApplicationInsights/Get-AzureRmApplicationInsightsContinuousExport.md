---
external help file: Microsoft.Azure.Commands.ApplicationInsights.dll-Help.xml
Module Name: AzureRM.ApplicationInsights
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.applicationinsights/get-azurermapplicationinsightscontinuousexport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApplicationInsights/Commands.ApplicationInsights/help/Get-AzureRmApplicationInsightsContinuousExport.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApplicationInsights/Commands.ApplicationInsights/help/Get-AzureRmApplicationInsightsContinuousExport.md
ms.openlocfilehash: 5e3b2feff3b59df30960856718911a3aeb699c37
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93548248"
---
# <span data-ttu-id="ca0eb-101">Get-AzureRmApplicationInsightsContinuousExport</span><span class="sxs-lookup"><span data-stu-id="ca0eb-101">Get-AzureRmApplicationInsightsContinuousExport</span></span>

## <span data-ttu-id="ca0eb-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="ca0eb-102">SYNOPSIS</span></span>
<span data-ttu-id="ca0eb-103">Uzyskiwanie ciągłej konfiguracji eksportu aplikacji Application Insights dla zasobu usługi Application Insights</span><span class="sxs-lookup"><span data-stu-id="ca0eb-103">Get application insights continuous export configuration for an application insights resource</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ca0eb-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="ca0eb-104">SYNTAX</span></span>

### <span data-ttu-id="ca0eb-105">ComponentNameParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="ca0eb-105">ComponentNameParameterSet (Default)</span></span>
```
Get-AzureRmApplicationInsightsContinuousExport [-ResourceGroupName] <String> [-Name] <String>
 [[-ExportId] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ca0eb-106">ComponentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="ca0eb-106">ComponentObjectParameterSet</span></span>
```
Get-AzureRmApplicationInsightsContinuousExport [-ApplicationInsightsComponent] <PSApplicationInsightsComponent>
 [[-ExportId] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ca0eb-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="ca0eb-107">ResourceIdParameterSet</span></span>
```
Get-AzureRmApplicationInsightsContinuousExport [-ResourceId] <String> [[-ExportId] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ca0eb-108">Opis</span><span class="sxs-lookup"><span data-stu-id="ca0eb-108">DESCRIPTION</span></span>
<span data-ttu-id="ca0eb-109">Uzyskiwanie ciągłej konfiguracji eksportu aplikacji Application Insights dla zasobu usługi Application Insights</span><span class="sxs-lookup"><span data-stu-id="ca0eb-109">Get application insights continuous export configuration for an application insights resource</span></span>

## <span data-ttu-id="ca0eb-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="ca0eb-110">EXAMPLES</span></span>

### <span data-ttu-id="ca0eb-111">Przykład 1 pobieranie ciągłego eksportu dla zasobu usługi Application Insights</span><span class="sxs-lookup"><span data-stu-id="ca0eb-111">Example 1 Get continuous export for an application insights resource</span></span>
```
PS C:\> Get-AzureRmApplicationInsightsContinuousExport -ResourceGroupName "testgroup" -Name "test"

ExportId                     DocumentTypes                ExportStatus DestinationStorageAccountId
--------                     -------------                ------------ ---------------------------
ZJrfffySPdtG3ESn3iRxVIEFuNY= Request, Performance Counter Preparing    /subscriptions/{subid}...
```

<span data-ttu-id="ca0eb-112">Uzyskiwanie ciągłych konfiguracji eksportu usługi Application Insights dla zasobu o nazwie "test" w grupie "testowanie"</span><span class="sxs-lookup"><span data-stu-id="ca0eb-112">Get application insights continuous export configurations for resource named "test" in resource group "testgroup"</span></span>

### <span data-ttu-id="ca0eb-113">Przykład 2 pobieranie ciągłego eksportu dla zasobu usługi Application Insights</span><span class="sxs-lookup"><span data-stu-id="ca0eb-113">Example 2 Get continuous export for an application insights resource</span></span>
```
PS C:\> Get-AzureRmApplicationInsightsContinuousExport -ResourceGroupName "testgroup" -Name "test" -ExportId "ZJrfffySPdtG3ESn3iRxVIEFuNY="

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

<span data-ttu-id="ca0eb-114">Uzyskiwanie ciągłej konfiguracji eksportu usługi Application Insights z identyfikatorem eksportu "ZJrfffySPdtG3ESn3iRxVIEFuNY =" dla zasobu o nazwie "test" w grupie "testowanie"</span><span class="sxs-lookup"><span data-stu-id="ca0eb-114">Get application insights continuous export configuration with export id "ZJrfffySPdtG3ESn3iRxVIEFuNY=" for resource named "test" in resource group "testgroup"</span></span>

## <span data-ttu-id="ca0eb-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="ca0eb-115">PARAMETERS</span></span>

### <span data-ttu-id="ca0eb-116">-ApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="ca0eb-116">-ApplicationInsightsComponent</span></span>
<span data-ttu-id="ca0eb-117">Obiekt składnika Application Insights.</span><span class="sxs-lookup"><span data-stu-id="ca0eb-117">Application Insights Component Object.</span></span>

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

### <span data-ttu-id="ca0eb-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ca0eb-118">-DefaultProfile</span></span>
<span data-ttu-id="ca0eb-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="ca0eb-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ca0eb-120">-ExportId</span><span class="sxs-lookup"><span data-stu-id="ca0eb-120">-ExportId</span></span>
<span data-ttu-id="ca0eb-121">Identyfikator eksportu w usłudze Application Insights.</span><span class="sxs-lookup"><span data-stu-id="ca0eb-121">Application Insights Continuous Export Id.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ca0eb-122">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="ca0eb-122">-Name</span></span>
<span data-ttu-id="ca0eb-123">Nazwa składnika Application Insights.</span><span class="sxs-lookup"><span data-stu-id="ca0eb-123">Application Insights Component Name.</span></span>

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

### <span data-ttu-id="ca0eb-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ca0eb-124">-ResourceGroupName</span></span>
<span data-ttu-id="ca0eb-125">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="ca0eb-125">Resource Group Name.</span></span>

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

### <span data-ttu-id="ca0eb-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ca0eb-126">-ResourceId</span></span>
<span data-ttu-id="ca0eb-127">Identyfikator zasobu składnika Application Insights.</span><span class="sxs-lookup"><span data-stu-id="ca0eb-127">Application Insights Component Resource Id.</span></span>

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

### <span data-ttu-id="ca0eb-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ca0eb-128">CommonParameters</span></span>
<span data-ttu-id="ca0eb-129">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ca0eb-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ca0eb-130">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ca0eb-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ca0eb-131">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ca0eb-131">INPUTS</span></span>

### <span data-ttu-id="ca0eb-132">System. String</span><span class="sxs-lookup"><span data-stu-id="ca0eb-132">System.String</span></span>

## <span data-ttu-id="ca0eb-133">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="ca0eb-133">OUTPUTS</span></span>

### <span data-ttu-id="ca0eb-134">Microsoft. Azure. Commands. ApplicationInsights. models. PSExportConfiguration</span><span class="sxs-lookup"><span data-stu-id="ca0eb-134">Microsoft.Azure.Commands.ApplicationInsights.Models.PSExportConfiguration</span></span>

## <span data-ttu-id="ca0eb-135">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="ca0eb-135">NOTES</span></span>

## <span data-ttu-id="ca0eb-136">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="ca0eb-136">RELATED LINKS</span></span>

