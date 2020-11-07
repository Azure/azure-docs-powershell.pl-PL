---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM.SiteRecovery
ms.assetid: A5697F1E-623A-4E26-96C8-6197852BFFAA
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Get-AzureRmSiteRecoveryVM.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Get-AzureRmSiteRecoveryVM.md
ms.openlocfilehash: 9f594b61b1ad34a39ea0a84381f6181cadc418c5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93717155"
---
# <span data-ttu-id="eda1a-101">Get-AzureRmSiteRecoveryVM</span><span class="sxs-lookup"><span data-stu-id="eda1a-101">Get-AzureRmSiteRecoveryVM</span></span>

## <span data-ttu-id="eda1a-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="eda1a-102">SYNOPSIS</span></span>
<span data-ttu-id="eda1a-103">Pobiera informacje o maszynach wirtualnych zarządzanych przez odzyskiwanie witryny.</span><span class="sxs-lookup"><span data-stu-id="eda1a-103">Gets information about Site Recovery-managed virtual machines.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="eda1a-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="eda1a-104">SYNTAX</span></span>

### <span data-ttu-id="eda1a-105">ByObject (domyślny)</span><span class="sxs-lookup"><span data-stu-id="eda1a-105">ByObject (Default)</span></span>
```
Get-AzureRmSiteRecoveryVM -ProtectionContainer <ASRProtectionContainer>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="eda1a-106">ByObjectWithName</span><span class="sxs-lookup"><span data-stu-id="eda1a-106">ByObjectWithName</span></span>
```
Get-AzureRmSiteRecoveryVM -Name <String> -ProtectionContainer <ASRProtectionContainer>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="eda1a-107">ByObjectWithFriendlyName</span><span class="sxs-lookup"><span data-stu-id="eda1a-107">ByObjectWithFriendlyName</span></span>
```
Get-AzureRmSiteRecoveryVM -FriendlyName <String> -ProtectionContainer <ASRProtectionContainer>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="eda1a-108">Opis</span><span class="sxs-lookup"><span data-stu-id="eda1a-108">DESCRIPTION</span></span>
<span data-ttu-id="eda1a-109">Polecenie cmdlet **Get-AzureRmSiteRecoveryVM** pobiera informacje o maszynach wirtualnych zarządzanych w usłudze Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="eda1a-109">The **Get-AzureRmSiteRecoveryVM** cmdlet gets information about virtual machines managed in Azure Site Recovery.</span></span>

## <span data-ttu-id="eda1a-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="eda1a-110">EXAMPLES</span></span>

## <span data-ttu-id="eda1a-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="eda1a-111">PARAMETERS</span></span>

### <span data-ttu-id="eda1a-112">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="eda1a-112">-FriendlyName</span></span>
<span data-ttu-id="eda1a-113">Określa przyjazną nazwę maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="eda1a-113">Specifies the friendly name of the virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: ByObjectWithFriendlyName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eda1a-114">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="eda1a-114">-Name</span></span>
<span data-ttu-id="eda1a-115">Określa nazwę maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="eda1a-115">Specifies the name of the virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: ByObjectWithName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eda1a-116">-ProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="eda1a-116">-ProtectionContainer</span></span>
<span data-ttu-id="eda1a-117">Określa obiekt kontenera ochrony przed odzyskiwaniem witryny.</span><span class="sxs-lookup"><span data-stu-id="eda1a-117">Specifies the Site Recovery protection container object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.SiteRecovery.ASRProtectionContainer
Parameter Sets: ByObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

```yaml
Type: Microsoft.Azure.Commands.SiteRecovery.ASRProtectionContainer
Parameter Sets: ByObjectWithName, ByObjectWithFriendlyName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="eda1a-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eda1a-118">-DefaultProfile</span></span>
<span data-ttu-id="eda1a-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="eda1a-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="eda1a-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eda1a-120">CommonParameters</span></span>
<span data-ttu-id="eda1a-121">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="eda1a-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eda1a-122">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="eda1a-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eda1a-123">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="eda1a-123">INPUTS</span></span>

### <span data-ttu-id="eda1a-124">ASRProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="eda1a-124">ASRProtectionContainer</span></span>
<span data-ttu-id="eda1a-125">Parametr "ProtectionContainer" akceptuje wartość typu "ASRProtectionContainer" z rurociągu</span><span class="sxs-lookup"><span data-stu-id="eda1a-125">Parameter 'ProtectionContainer' accepts value of type 'ASRProtectionContainer' from the pipeline</span></span>

### <span data-ttu-id="eda1a-126">ASRProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="eda1a-126">ASRProtectionContainer</span></span>
<span data-ttu-id="eda1a-127">Parametr "ProtectionContainer" akceptuje wartość typu "ASRProtectionContainer" z rurociągu</span><span class="sxs-lookup"><span data-stu-id="eda1a-127">Parameter 'ProtectionContainer' accepts value of type 'ASRProtectionContainer' from the pipeline</span></span>

## <span data-ttu-id="eda1a-128">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="eda1a-128">OUTPUTS</span></span>

### <span data-ttu-id="eda1a-129">System. Collections. Generic. IEnumerable ' 1 [Microsoft. Azure. Commands. SiteRecovery. ASRVirtualMachine]</span><span class="sxs-lookup"><span data-stu-id="eda1a-129">System.Collections.Generic.IEnumerable\`1[Microsoft.Azure.Commands.SiteRecovery.ASRVirtualMachine]</span></span>

## <span data-ttu-id="eda1a-130">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="eda1a-130">NOTES</span></span>

## <span data-ttu-id="eda1a-131">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="eda1a-131">RELATED LINKS</span></span>

[<span data-ttu-id="eda1a-132">Set-AzureRmSiteRecoveryVM</span><span class="sxs-lookup"><span data-stu-id="eda1a-132">Set-AzureRmSiteRecoveryVM</span></span>](./Set-AzureRmSiteRecoveryVM.md)
