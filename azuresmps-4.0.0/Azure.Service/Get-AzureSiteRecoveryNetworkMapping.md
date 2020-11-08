---
external help file: Microsoft.Azure.Commands.RecoveryServicesRdfe.dll-Help.xml
ms.assetid: F6C01C25-655C-4798-9826-F7CB168181C7
online version: ''
schema: 2.0.0
ms.openlocfilehash: bc8b7dc7e23a98111e75c2b2c9c079f010e3c5dc
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94054556"
---
# <span data-ttu-id="935f7-101">Get-AzureSiteRecoveryNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="935f7-101">Get-AzureSiteRecoveryNetworkMapping</span></span>

## <span data-ttu-id="935f7-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="935f7-102">SYNOPSIS</span></span>
<span data-ttu-id="935f7-103">Pobiera mapowania sieci dla magazynu odzyskiwania witryny.</span><span class="sxs-lookup"><span data-stu-id="935f7-103">Gets network mappings for a Site Recovery vault.</span></span>

## <span data-ttu-id="935f7-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="935f7-104">SYNTAX</span></span>

### <span data-ttu-id="935f7-105">EnterpriseToEnterprise</span><span class="sxs-lookup"><span data-stu-id="935f7-105">EnterpriseToEnterprise</span></span>
```
Get-AzureSiteRecoveryNetworkMapping -PrimaryServer <ASRServer> -RecoveryServer <ASRServer>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="935f7-106">EnterpriseToAzure</span><span class="sxs-lookup"><span data-stu-id="935f7-106">EnterpriseToAzure</span></span>
```
Get-AzureSiteRecoveryNetworkMapping -PrimaryServer <ASRServer> [-Azure] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="935f7-107">Opis</span><span class="sxs-lookup"><span data-stu-id="935f7-107">DESCRIPTION</span></span>
<span data-ttu-id="935f7-108">Polecenie cmdlet **Get-AzureSiteRecoveryNetworkMapping** pobiera informacje o mapowaniach sieciowych usługi Azure Site Recovery dla bieżącego magazynu odzyskiwania witryny.</span><span class="sxs-lookup"><span data-stu-id="935f7-108">The **Get-AzureSiteRecoveryNetworkMapping** cmdlet gets information about Azure Site Recovery network mappings for the current Site Recovery vault.</span></span>

## <span data-ttu-id="935f7-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="935f7-109">EXAMPLES</span></span>

### <span data-ttu-id="935f7-110">Przykład 1: uzyskiwanie mapowania między siecią a siecią odzyskiwania</span><span class="sxs-lookup"><span data-stu-id="935f7-110">Example 1: Get the mapping between a network and a recovery network</span></span>
```
PS C:\> $Servers = Get-AzureSiteRecoveryServer
PS C:\> Get-AzureSiteRecoveryNetworkMapping -PrimaryServer $Servers[0] -RecoveryServer $Servers[0]
PrimaryServerId     : 774859b0-1966-48cc-9df7-759c441b7a8c
PrimaryNetworkId    : 7cfd636e-5cc2-4e01-873b-8a7aa4962341
PrimaryNetworkName  : phase2RecoveryVMNetwork
RecoveryServerId    : 774859b0-1966-48cc-9df7-759c441b7a8c
RecoveryNetworkId   : d903e2c6-3141-4cef-bfe1-04616cd43cbb
RecoveryNetworkName : phase2PrimaryVMNetwork
PairingStatus       : OK
```

<span data-ttu-id="935f7-111">Pierwsze polecenie cmdlet pobiera serwery dla bieżącego magazynu usługi Azure Site Recovery, korzystając z polecenia cmdlet **Get-AzureSiteRecoveryServer** .</span><span class="sxs-lookup"><span data-stu-id="935f7-111">The first command cmdlet gets servers for the current Azure Site Recovery vault by using the **Get-AzureSiteRecoveryServer** cmdlet.</span></span>
<span data-ttu-id="935f7-112">Polecenie zapisuje serwery odzyskiwania witryny w zmiennej tablicy $Servers.</span><span class="sxs-lookup"><span data-stu-id="935f7-112">The command stores the Site Recovery servers in the $Servers array variable.</span></span>

<span data-ttu-id="935f7-113">Drugie polecenie uzyskuje mapowanie między siecią podstawową a siecią odzyskiwania.</span><span class="sxs-lookup"><span data-stu-id="935f7-113">The second command gets the mapping between the primary network and the recovery network.</span></span>
<span data-ttu-id="935f7-114">Polecenie Określa podstawowy serwer mapowania sieci jako pierwszy element $Servers.</span><span class="sxs-lookup"><span data-stu-id="935f7-114">The command specifies the primary server for the network mapping as the first element of $Servers.</span></span>
<span data-ttu-id="935f7-115">To polecenie Określa serwer sieci odzyskiwania jako drugi element $Servers.</span><span class="sxs-lookup"><span data-stu-id="935f7-115">The command specifies the server for the recovery network as the second element of $Servers.</span></span>

### <span data-ttu-id="935f7-116">Przykład 2: uzyskiwanie mapowania między siecią a siecią maszyny wirtualnej platformy Azure</span><span class="sxs-lookup"><span data-stu-id="935f7-116">Example 2: Get the mapping between a network and an Azure virtual machine network</span></span>
```
PS C:\> $Servers = Get-AzureSiteRecoveryServer
PS C:\> Get-AzureSiteRecoveryNetworkMapping -Azure -PrimaryServer $Servers[0] 
PrimaryServerId     : 774859b0-1966-48cc-9df7-759c441b7a8c
PrimaryNetworkId    : 7cfd636e-5cc2-4e01-873b-8a7aa4962341
PrimaryNetworkName  : phase2RecoveryVMNetwork
RecoveryServerId    : 21a9403c-6ec1-44f2-b744-b4e50b792387
RecoveryNetworkId   : ecb3a462-664f-4f57-873e-d09b5925e1a1
RecoveryNetworkName : AzureVMNetwork
PairingStatus       : OK
```

<span data-ttu-id="935f7-117">Pierwsze polecenie cmdlet pobiera serwery dla bieżącego magazynu odzyskiwania witryny.</span><span class="sxs-lookup"><span data-stu-id="935f7-117">The first command cmdlet gets servers for the current Site Recovery vault.</span></span>
<span data-ttu-id="935f7-118">Polecenie zapisuje serwery w zmiennej tablicowej $Servers.</span><span class="sxs-lookup"><span data-stu-id="935f7-118">The command stores the servers in the $Servers array variable.</span></span>

<span data-ttu-id="935f7-119">Drugie polecenie uzyskuje mapowanie między siecią podstawową a siecią maszyny wirtualnej Azure.</span><span class="sxs-lookup"><span data-stu-id="935f7-119">The second command gets a mapping between the primary network and an Azure virtual machine network.</span></span>
<span data-ttu-id="935f7-120">Polecenie Określa serwer podstawowy dla sieci jako pierwszy element $Servers.</span><span class="sxs-lookup"><span data-stu-id="935f7-120">The command specifies the primary server for the network as the first element of $Servers.</span></span>
<span data-ttu-id="935f7-121">Polecenie określa parametr *platformy Azure* .</span><span class="sxs-lookup"><span data-stu-id="935f7-121">The command specifies the *Azure* parameter.</span></span>
<span data-ttu-id="935f7-122">Dlatego polecenie uzyskuje mapowanie do sieci maszyny wirtualnej platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="935f7-122">Therefore, the command gets the mapping to an Azure virtual machine network.</span></span>

## <span data-ttu-id="935f7-123">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="935f7-123">PARAMETERS</span></span>

### <span data-ttu-id="935f7-124">-Azure</span><span class="sxs-lookup"><span data-stu-id="935f7-124">-Azure</span></span>
<span data-ttu-id="935f7-125">Wskazuje, że to polecenie cmdlet pobiera mapowania sieci dla sieci na serwerze podstawowym zamapowanym na wirtualne sieci Azure.</span><span class="sxs-lookup"><span data-stu-id="935f7-125">Indicates that this cmdlet gets network mappings for networks on the primary server mapped to Azure virtual networks.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: EnterpriseToAzure
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="935f7-126">-PrimaryServer</span><span class="sxs-lookup"><span data-stu-id="935f7-126">-PrimaryServer</span></span>
<span data-ttu-id="935f7-127">Określa serwer podstawowy, dla którego mają być uzyskiwane mapowania.</span><span class="sxs-lookup"><span data-stu-id="935f7-127">Specifies a primary server for which to get mappings.</span></span>

```yaml
Type: ASRServer
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="935f7-128">-Profile</span><span class="sxs-lookup"><span data-stu-id="935f7-128">-Profile</span></span>
<span data-ttu-id="935f7-129">Określa Profil platformy Azure, na podstawie którego jest odczytywane to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="935f7-129">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="935f7-130">Jeśli nie podano profilu, to polecenie cmdlet odczytuje lokalny profil domyślny.</span><span class="sxs-lookup"><span data-stu-id="935f7-130">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="935f7-131">-RecoveryServer</span><span class="sxs-lookup"><span data-stu-id="935f7-131">-RecoveryServer</span></span>
<span data-ttu-id="935f7-132">Określa serwer odzyskiwania, dla którego mają być uzyskiwane mapowania.</span><span class="sxs-lookup"><span data-stu-id="935f7-132">Specifies a recovery server for which to get mappings.</span></span>

```yaml
Type: ASRServer
Parameter Sets: EnterpriseToEnterprise
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="935f7-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="935f7-133">CommonParameters</span></span>
<span data-ttu-id="935f7-134">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="935f7-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="935f7-135">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="935f7-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="935f7-136">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="935f7-136">INPUTS</span></span>

## <span data-ttu-id="935f7-137">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="935f7-137">OUTPUTS</span></span>

## <span data-ttu-id="935f7-138">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="935f7-138">NOTES</span></span>

## <span data-ttu-id="935f7-139">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="935f7-139">RELATED LINKS</span></span>

[<span data-ttu-id="935f7-140">Nowe — AzureSiteRecoveryNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="935f7-140">New-AzureSiteRecoveryNetworkMapping</span></span>](./New-AzureSiteRecoveryNetworkMapping.md)

[<span data-ttu-id="935f7-141">Remove-AzureSiteRecoveryNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="935f7-141">Remove-AzureSiteRecoveryNetworkMapping</span></span>](./Remove-AzureSiteRecoveryNetworkMapping.md)


