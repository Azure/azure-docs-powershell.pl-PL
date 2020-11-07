---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM
ms.assetid: 4CC5E6A8-B51A-49ED-BB93-FE63F1500780
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.siterecovery/get-azurermsiterecoverynetwork
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Get-AzureRmSiteRecoveryNetwork.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Get-AzureRmSiteRecoveryNetwork.md
ms.openlocfilehash: 6ffd3a295ecc228ec395a00ba597f2d7b0967a2e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93716981"
---
# <span data-ttu-id="4f105-101">Get-AzureRmSiteRecoveryNetwork</span><span class="sxs-lookup"><span data-stu-id="4f105-101">Get-AzureRmSiteRecoveryNetwork</span></span>

## <span data-ttu-id="4f105-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="4f105-102">SYNOPSIS</span></span>
<span data-ttu-id="4f105-103">Pobiera informacje o sieciach zarządzanych przez odzyskiwanie witryny dla bieżącego magazynu.</span><span class="sxs-lookup"><span data-stu-id="4f105-103">Gets information about the networks managed by Site Recovery for the current vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4f105-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="4f105-104">SYNTAX</span></span>

### <span data-ttu-id="4f105-105">Domyślne (domyślnie)</span><span class="sxs-lookup"><span data-stu-id="4f105-105">Default (Default)</span></span>
```
Get-AzureRmSiteRecoveryNetwork [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4f105-106">ByServerObject</span><span class="sxs-lookup"><span data-stu-id="4f105-106">ByServerObject</span></span>
```
Get-AzureRmSiteRecoveryNetwork -Server <ASRServer> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="4f105-107">ByNameLegacy</span><span class="sxs-lookup"><span data-stu-id="4f105-107">ByNameLegacy</span></span>
```
Get-AzureRmSiteRecoveryNetwork -Server <ASRServer> -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="4f105-108">ByFriendlyNameLegacy</span><span class="sxs-lookup"><span data-stu-id="4f105-108">ByFriendlyNameLegacy</span></span>
```
Get-AzureRmSiteRecoveryNetwork -Server <ASRServer> -FriendlyName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4f105-109">ByFabricObject</span><span class="sxs-lookup"><span data-stu-id="4f105-109">ByFabricObject</span></span>
```
Get-AzureRmSiteRecoveryNetwork -Fabric <ASRFabric> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="4f105-110">ByName</span><span class="sxs-lookup"><span data-stu-id="4f105-110">ByName</span></span>
```
Get-AzureRmSiteRecoveryNetwork -Fabric <ASRFabric> -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="4f105-111">ByFriendlyName</span><span class="sxs-lookup"><span data-stu-id="4f105-111">ByFriendlyName</span></span>
```
Get-AzureRmSiteRecoveryNetwork -Fabric <ASRFabric> -FriendlyName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4f105-112">Opis</span><span class="sxs-lookup"><span data-stu-id="4f105-112">DESCRIPTION</span></span>
<span data-ttu-id="4f105-113">Polecenie cmdlet **Get-AzureRmSiteRecoveryNetwork** pobiera informacje o sieciach usługi Azure Site Recovery dla bieżącego magazynu usługi Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="4f105-113">The **Get-AzureRmSiteRecoveryNetwork** cmdlet gets information about Azure Site Recovery networks for the current Azure Site Recovery vault.</span></span>

## <span data-ttu-id="4f105-114">Przykłady</span><span class="sxs-lookup"><span data-stu-id="4f105-114">EXAMPLES</span></span>

## <span data-ttu-id="4f105-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="4f105-115">PARAMETERS</span></span>

### <span data-ttu-id="4f105-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4f105-116">-DefaultProfile</span></span>
<span data-ttu-id="4f105-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="4f105-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4f105-118">-Fabric</span><span class="sxs-lookup"><span data-stu-id="4f105-118">-Fabric</span></span>
```yaml
Type: ASRFabric
Parameter Sets: ByFabricObject, ByName, ByFriendlyName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4f105-119">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="4f105-119">-FriendlyName</span></span>
<span data-ttu-id="4f105-120">Określa przyjazną nazwę sieci maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="4f105-120">Specifies the friendly name of the virtual machine network.</span></span>

```yaml
Type: String
Parameter Sets: ByFriendlyNameLegacy
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: ByFriendlyName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4f105-121">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="4f105-121">-Name</span></span>
<span data-ttu-id="4f105-122">Określa nazwę sieci maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="4f105-122">Specifies the name of the virtual machine network.</span></span>

```yaml
Type: String
Parameter Sets: ByNameLegacy
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: ByName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4f105-123">-Server</span><span class="sxs-lookup"><span data-stu-id="4f105-123">-Server</span></span>
```yaml
Type: ASRServer
Parameter Sets: ByServerObject, ByNameLegacy, ByFriendlyNameLegacy
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4f105-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4f105-124">CommonParameters</span></span>
<span data-ttu-id="4f105-125">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4f105-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4f105-126">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4f105-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4f105-127">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="4f105-127">INPUTS</span></span>

### <span data-ttu-id="4f105-128">ASRFabric</span><span class="sxs-lookup"><span data-stu-id="4f105-128">ASRFabric</span></span>
<span data-ttu-id="4f105-129">Parametr "Fabric" akceptuje wartość typu "ASRFabric" z procesu</span><span class="sxs-lookup"><span data-stu-id="4f105-129">Parameter 'Fabric' accepts value of type 'ASRFabric' from the pipeline</span></span>

### <span data-ttu-id="4f105-130">Ciąg</span><span class="sxs-lookup"><span data-stu-id="4f105-130">String</span></span>
<span data-ttu-id="4f105-131">Parametr "FriendlyName" akceptuje wartość typu "String" z procesu</span><span class="sxs-lookup"><span data-stu-id="4f105-131">Parameter 'FriendlyName' accepts value of type 'String' from the pipeline</span></span>

### <span data-ttu-id="4f105-132">Ciąg</span><span class="sxs-lookup"><span data-stu-id="4f105-132">String</span></span>
<span data-ttu-id="4f105-133">Parametr "FriendlyName" akceptuje wartość typu "String" z procesu</span><span class="sxs-lookup"><span data-stu-id="4f105-133">Parameter 'FriendlyName' accepts value of type 'String' from the pipeline</span></span>

### <span data-ttu-id="4f105-134">Ciąg</span><span class="sxs-lookup"><span data-stu-id="4f105-134">String</span></span>
<span data-ttu-id="4f105-135">Parametr "nazwa" akceptuje wartość typu "String" z procesu</span><span class="sxs-lookup"><span data-stu-id="4f105-135">Parameter 'Name' accepts value of type 'String' from the pipeline</span></span>

### <span data-ttu-id="4f105-136">Ciąg</span><span class="sxs-lookup"><span data-stu-id="4f105-136">String</span></span>
<span data-ttu-id="4f105-137">Parametr "nazwa" akceptuje wartość typu "String" z procesu</span><span class="sxs-lookup"><span data-stu-id="4f105-137">Parameter 'Name' accepts value of type 'String' from the pipeline</span></span>

### <span data-ttu-id="4f105-138">ASRServer</span><span class="sxs-lookup"><span data-stu-id="4f105-138">ASRServer</span></span>
<span data-ttu-id="4f105-139">Parametr "serwer" akceptuje wartość typu "ASRServer" z procesu</span><span class="sxs-lookup"><span data-stu-id="4f105-139">Parameter 'Server' accepts value of type 'ASRServer' from the pipeline</span></span>

## <span data-ttu-id="4f105-140">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="4f105-140">OUTPUTS</span></span>

### <span data-ttu-id="4f105-141">System. Collections. Generic. IEnumerable ' 1 [Microsoft. Azure. Commands. SiteRecovery. ASRNetwork]</span><span class="sxs-lookup"><span data-stu-id="4f105-141">System.Collections.Generic.IEnumerable\`1[Microsoft.Azure.Commands.SiteRecovery.ASRNetwork]</span></span>

## <span data-ttu-id="4f105-142">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="4f105-142">NOTES</span></span>

## <span data-ttu-id="4f105-143">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="4f105-143">RELATED LINKS</span></span>

