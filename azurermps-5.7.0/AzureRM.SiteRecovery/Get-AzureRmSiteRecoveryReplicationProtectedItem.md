---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM
ms.assetid: 99196F44-F1DB-4219-91C0-3056624ADE5B
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.siterecovery/get-azurermsiterecoveryreplicationprotecteditem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Get-AzureRmSiteRecoveryReplicationProtectedItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Get-AzureRmSiteRecoveryReplicationProtectedItem.md
ms.openlocfilehash: 210b8ca6d8165049edc190e24e4a435046e1461e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93718450"
---
# <span data-ttu-id="71e89-101">Get-AzureRmSiteRecoveryReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="71e89-101">Get-AzureRmSiteRecoveryReplicationProtectedItem</span></span>

## <span data-ttu-id="71e89-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="71e89-102">SYNOPSIS</span></span>
<span data-ttu-id="71e89-103">Pobiera właściwości elementów chronionych przy odzyskiwaniu witryny Azure.</span><span class="sxs-lookup"><span data-stu-id="71e89-103">Gets the properties of Azure Site Recovery Protected Items.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="71e89-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="71e89-104">SYNTAX</span></span>

### <span data-ttu-id="71e89-105">ByObject (domyślny)</span><span class="sxs-lookup"><span data-stu-id="71e89-105">ByObject (Default)</span></span>
```
Get-AzureRmSiteRecoveryReplicationProtectedItem -ProtectionContainer <ASRProtectionContainer>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="71e89-106">ByObjectWithName</span><span class="sxs-lookup"><span data-stu-id="71e89-106">ByObjectWithName</span></span>
```
Get-AzureRmSiteRecoveryReplicationProtectedItem -Name <String> -ProtectionContainer <ASRProtectionContainer>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="71e89-107">ByObjectWithFriendlyName</span><span class="sxs-lookup"><span data-stu-id="71e89-107">ByObjectWithFriendlyName</span></span>
```
Get-AzureRmSiteRecoveryReplicationProtectedItem -FriendlyName <String>
 -ProtectionContainer <ASRProtectionContainer> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="71e89-108">ByProtectableItemObject</span><span class="sxs-lookup"><span data-stu-id="71e89-108">ByProtectableItemObject</span></span>
```
Get-AzureRmSiteRecoveryReplicationProtectedItem -ProtectableItem <ASRProtectableItem>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="71e89-109">Opis</span><span class="sxs-lookup"><span data-stu-id="71e89-109">DESCRIPTION</span></span>
<span data-ttu-id="71e89-110">Polecenie cmdlet **Get-AzureRmSiteRecoveryReplicationProtectedItem** pobiera właściwości elementów chronionych przy odzyskiwaniu witryny Azure.</span><span class="sxs-lookup"><span data-stu-id="71e89-110">The **Get-AzureRmSiteRecoveryReplicationProtectedItem** cmdlet gets the properties of Azure Site Recovery Protected Items.</span></span>

## <span data-ttu-id="71e89-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="71e89-111">EXAMPLES</span></span>

## <span data-ttu-id="71e89-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="71e89-112">PARAMETERS</span></span>

### <span data-ttu-id="71e89-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="71e89-113">-DefaultProfile</span></span>
<span data-ttu-id="71e89-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="71e89-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="71e89-115">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="71e89-115">-FriendlyName</span></span>
<span data-ttu-id="71e89-116">Określa przyjazną nazwę elementu chronionego replikacją, który jest pobierany przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="71e89-116">Specifies the friendly name of the Replication Protected Item that this cmdlet gets.</span></span>

```yaml
Type: String
Parameter Sets: ByObjectWithFriendlyName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="71e89-117">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="71e89-117">-Name</span></span>
<span data-ttu-id="71e89-118">Określa nazwę elementu chronionego replikacją, który jest pobierany przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="71e89-118">Specifies the name of the Replication Protected Item that this cmdlet gets.</span></span>

```yaml
Type: String
Parameter Sets: ByObjectWithName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="71e89-119">-ProtectableItem</span><span class="sxs-lookup"><span data-stu-id="71e89-119">-ProtectableItem</span></span>
<span data-ttu-id="71e89-120">Określa element chroniony, odpowiadający elementowi chronionej replikacji.</span><span class="sxs-lookup"><span data-stu-id="71e89-120">Specifies the Protectable Item corresponding to the Replication Protected Item.</span></span>

```yaml
Type: ASRProtectableItem
Parameter Sets: ByProtectableItemObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="71e89-121">-ProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="71e89-121">-ProtectionContainer</span></span>
<span data-ttu-id="71e89-122">Określa obiekt kontenera ochrony przed odzyskiwaniem witryny Azure.</span><span class="sxs-lookup"><span data-stu-id="71e89-122">Specifies the Azure Site Recovery Protection Container object.</span></span>

```yaml
Type: ASRProtectionContainer
Parameter Sets: ByObject, ByObjectWithName, ByObjectWithFriendlyName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="71e89-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="71e89-123">CommonParameters</span></span>
<span data-ttu-id="71e89-124">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="71e89-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="71e89-125">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="71e89-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="71e89-126">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="71e89-126">INPUTS</span></span>

### <span data-ttu-id="71e89-127">ASRProtectableItem</span><span class="sxs-lookup"><span data-stu-id="71e89-127">ASRProtectableItem</span></span>
<span data-ttu-id="71e89-128">Parametr "ProtectableItem" akceptuje wartość typu "ASRProtectableItem" z rurociągu</span><span class="sxs-lookup"><span data-stu-id="71e89-128">Parameter 'ProtectableItem' accepts value of type 'ASRProtectableItem' from the pipeline</span></span>

### <span data-ttu-id="71e89-129">ASRProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="71e89-129">ASRProtectionContainer</span></span>
<span data-ttu-id="71e89-130">Parametr "ProtectionContainer" akceptuje wartość typu "ASRProtectionContainer" z rurociągu</span><span class="sxs-lookup"><span data-stu-id="71e89-130">Parameter 'ProtectionContainer' accepts value of type 'ASRProtectionContainer' from the pipeline</span></span>

## <span data-ttu-id="71e89-131">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="71e89-131">OUTPUTS</span></span>

### <span data-ttu-id="71e89-132">System. Collections. Generic. IEnumerable ' 1 [[Microsoft. Azure. Commands. SiteRecovery. ASRReplicationProtectedItem, Microsoft. Azure. Commands. SiteRecovery, Version = 2.0.1.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="71e89-132">System.Collections.Generic.IEnumerable\`1[[Microsoft.Azure.Commands.SiteRecovery.ASRReplicationProtectedItem, Microsoft.Azure.Commands.SiteRecovery, Version=2.0.1.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="71e89-133">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="71e89-133">NOTES</span></span>

## <span data-ttu-id="71e89-134">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="71e89-134">RELATED LINKS</span></span>

[<span data-ttu-id="71e89-135">Nowe — AzureRmSiteRecoveryReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="71e89-135">New-AzureRmSiteRecoveryReplicationProtectedItem</span></span>](./New-AzureRmSiteRecoveryReplicationProtectedItem.md)

[<span data-ttu-id="71e89-136">Remove-AzureRmSiteRecoveryReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="71e89-136">Remove-AzureRmSiteRecoveryReplicationProtectedItem</span></span>](./Remove-AzureRmSiteRecoveryReplicationProtectedItem.md)

[<span data-ttu-id="71e89-137">Set-AzureRmSiteRecoveryReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="71e89-137">Set-AzureRmSiteRecoveryReplicationProtectedItem</span></span>](./Set-AzureRmSiteRecoveryReplicationProtectedItem.md)
