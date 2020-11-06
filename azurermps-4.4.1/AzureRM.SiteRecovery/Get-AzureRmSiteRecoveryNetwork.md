---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM.SiteRecovery
ms.assetid: 4CC5E6A8-B51A-49ED-BB93-FE63F1500780
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Get-AzureRmSiteRecoveryNetwork.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Get-AzureRmSiteRecoveryNetwork.md
ms.openlocfilehash: 83410371d517bbd90a0b302d258ff25325e06cf9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93542911"
---
# <span data-ttu-id="cf3c9-101">Get-AzureRmSiteRecoveryNetwork</span><span class="sxs-lookup"><span data-stu-id="cf3c9-101">Get-AzureRmSiteRecoveryNetwork</span></span>

## <span data-ttu-id="cf3c9-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="cf3c9-102">SYNOPSIS</span></span>
<span data-ttu-id="cf3c9-103">Pobiera informacje o sieciach zarządzanych przez odzyskiwanie witryny dla bieżącego magazynu.</span><span class="sxs-lookup"><span data-stu-id="cf3c9-103">Gets information about the networks managed by Site Recovery for the current vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="cf3c9-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="cf3c9-104">SYNTAX</span></span>

### <span data-ttu-id="cf3c9-105">Domyślne (domyślnie)</span><span class="sxs-lookup"><span data-stu-id="cf3c9-105">Default (Default)</span></span>
```
Get-AzureRmSiteRecoveryNetwork [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="cf3c9-106">ByServerObject</span><span class="sxs-lookup"><span data-stu-id="cf3c9-106">ByServerObject</span></span>
```
Get-AzureRmSiteRecoveryNetwork -Server <ASRServer> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="cf3c9-107">ByNameLegacy</span><span class="sxs-lookup"><span data-stu-id="cf3c9-107">ByNameLegacy</span></span>
```
Get-AzureRmSiteRecoveryNetwork -Server <ASRServer> -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="cf3c9-108">ByFriendlyNameLegacy</span><span class="sxs-lookup"><span data-stu-id="cf3c9-108">ByFriendlyNameLegacy</span></span>
```
Get-AzureRmSiteRecoveryNetwork -Server <ASRServer> -FriendlyName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="cf3c9-109">ByFabricObject</span><span class="sxs-lookup"><span data-stu-id="cf3c9-109">ByFabricObject</span></span>
```
Get-AzureRmSiteRecoveryNetwork -Fabric <ASRFabric> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="cf3c9-110">ByName</span><span class="sxs-lookup"><span data-stu-id="cf3c9-110">ByName</span></span>
```
Get-AzureRmSiteRecoveryNetwork -Fabric <ASRFabric> -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="cf3c9-111">ByFriendlyName</span><span class="sxs-lookup"><span data-stu-id="cf3c9-111">ByFriendlyName</span></span>
```
Get-AzureRmSiteRecoveryNetwork -Fabric <ASRFabric> -FriendlyName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="cf3c9-112">Opis</span><span class="sxs-lookup"><span data-stu-id="cf3c9-112">DESCRIPTION</span></span>
<span data-ttu-id="cf3c9-113">Polecenie cmdlet **Get-AzureRmSiteRecoveryNetwork** pobiera informacje o sieciach usługi Azure Site Recovery dla bieżącego magazynu usługi Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="cf3c9-113">The **Get-AzureRmSiteRecoveryNetwork** cmdlet gets information about Azure Site Recovery networks for the current Azure Site Recovery vault.</span></span>

## <span data-ttu-id="cf3c9-114">Przykłady</span><span class="sxs-lookup"><span data-stu-id="cf3c9-114">EXAMPLES</span></span>

## <span data-ttu-id="cf3c9-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="cf3c9-115">PARAMETERS</span></span>

### <span data-ttu-id="cf3c9-116">-Fabric</span><span class="sxs-lookup"><span data-stu-id="cf3c9-116">-Fabric</span></span>
```yaml
Type: Microsoft.Azure.Commands.SiteRecovery.ASRFabric
Parameter Sets: ByFabricObject, ByName, ByFriendlyName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="cf3c9-117">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="cf3c9-117">-FriendlyName</span></span>
<span data-ttu-id="cf3c9-118">Określa przyjazną nazwę sieci maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="cf3c9-118">Specifies the friendly name of the virtual machine network.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFriendlyNameLegacy
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ByFriendlyName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="cf3c9-119">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="cf3c9-119">-Name</span></span>
<span data-ttu-id="cf3c9-120">Określa nazwę sieci maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="cf3c9-120">Specifies the name of the virtual machine network.</span></span>

```yaml
Type: System.String
Parameter Sets: ByNameLegacy
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ByName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="cf3c9-121">-Server</span><span class="sxs-lookup"><span data-stu-id="cf3c9-121">-Server</span></span>
```yaml
Type: Microsoft.Azure.Commands.SiteRecovery.ASRServer
Parameter Sets: ByServerObject, ByNameLegacy, ByFriendlyNameLegacy
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="cf3c9-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cf3c9-122">-DefaultProfile</span></span>
<span data-ttu-id="cf3c9-123">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="cf3c9-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="cf3c9-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cf3c9-124">CommonParameters</span></span>
<span data-ttu-id="cf3c9-125">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cf3c9-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cf3c9-126">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cf3c9-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cf3c9-127">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="cf3c9-127">INPUTS</span></span>

### <span data-ttu-id="cf3c9-128">ASRFabric</span><span class="sxs-lookup"><span data-stu-id="cf3c9-128">ASRFabric</span></span>
<span data-ttu-id="cf3c9-129">Parametr "Fabric" akceptuje wartość typu "ASRFabric" z procesu</span><span class="sxs-lookup"><span data-stu-id="cf3c9-129">Parameter 'Fabric' accepts value of type 'ASRFabric' from the pipeline</span></span>

### <span data-ttu-id="cf3c9-130">Ciąg</span><span class="sxs-lookup"><span data-stu-id="cf3c9-130">String</span></span>
<span data-ttu-id="cf3c9-131">Parametr "FriendlyName" akceptuje wartość typu "String" z procesu</span><span class="sxs-lookup"><span data-stu-id="cf3c9-131">Parameter 'FriendlyName' accepts value of type 'String' from the pipeline</span></span>

### <span data-ttu-id="cf3c9-132">Ciąg</span><span class="sxs-lookup"><span data-stu-id="cf3c9-132">String</span></span>
<span data-ttu-id="cf3c9-133">Parametr "FriendlyName" akceptuje wartość typu "String" z procesu</span><span class="sxs-lookup"><span data-stu-id="cf3c9-133">Parameter 'FriendlyName' accepts value of type 'String' from the pipeline</span></span>

### <span data-ttu-id="cf3c9-134">Ciąg</span><span class="sxs-lookup"><span data-stu-id="cf3c9-134">String</span></span>
<span data-ttu-id="cf3c9-135">Parametr "nazwa" akceptuje wartość typu "String" z procesu</span><span class="sxs-lookup"><span data-stu-id="cf3c9-135">Parameter 'Name' accepts value of type 'String' from the pipeline</span></span>

### <span data-ttu-id="cf3c9-136">Ciąg</span><span class="sxs-lookup"><span data-stu-id="cf3c9-136">String</span></span>
<span data-ttu-id="cf3c9-137">Parametr "nazwa" akceptuje wartość typu "String" z procesu</span><span class="sxs-lookup"><span data-stu-id="cf3c9-137">Parameter 'Name' accepts value of type 'String' from the pipeline</span></span>

### <span data-ttu-id="cf3c9-138">ASRServer</span><span class="sxs-lookup"><span data-stu-id="cf3c9-138">ASRServer</span></span>
<span data-ttu-id="cf3c9-139">Parametr "serwer" akceptuje wartość typu "ASRServer" z procesu</span><span class="sxs-lookup"><span data-stu-id="cf3c9-139">Parameter 'Server' accepts value of type 'ASRServer' from the pipeline</span></span>

## <span data-ttu-id="cf3c9-140">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="cf3c9-140">OUTPUTS</span></span>

### <span data-ttu-id="cf3c9-141">System. Collections. Generic. IEnumerable ' 1 [Microsoft. Azure. Commands. SiteRecovery. ASRNetwork]</span><span class="sxs-lookup"><span data-stu-id="cf3c9-141">System.Collections.Generic.IEnumerable\`1[Microsoft.Azure.Commands.SiteRecovery.ASRNetwork]</span></span>

## <span data-ttu-id="cf3c9-142">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="cf3c9-142">NOTES</span></span>

## <span data-ttu-id="cf3c9-143">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="cf3c9-143">RELATED LINKS</span></span>

