---
external help file: Microsoft.Azure.Commands.AzureBackup.dll-Help.xml
Module Name: AzureRM.Backup
ms.assetid: 394500DB-D2BB-4793-8D9F-2CAF4D892A55
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.backup/register-azurermbackupcontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Register-AzureRmBackupContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Register-AzureRmBackupContainer.md
ms.openlocfilehash: 71c7d883994897e4dc4b450391fb50949a125c77
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93550656"
---
# <span data-ttu-id="c5470-101">Register-AzureRmBackupContainer</span><span class="sxs-lookup"><span data-stu-id="c5470-101">Register-AzureRmBackupContainer</span></span>

## <span data-ttu-id="c5470-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="c5470-102">SYNOPSIS</span></span>
<span data-ttu-id="c5470-103">Rejestruje kontener z magazynem kopii zapasowej.</span><span class="sxs-lookup"><span data-stu-id="c5470-103">Registers the container with a Backup vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c5470-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="c5470-104">SYNTAX</span></span>

### <span data-ttu-id="c5470-105">V1VM</span><span class="sxs-lookup"><span data-stu-id="c5470-105">V1VM</span></span>
```
Register-AzureRmBackupContainer -Name <String> -ServiceName <String> [-Vault] <AzureRMBackupVault>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c5470-106">V2VM</span><span class="sxs-lookup"><span data-stu-id="c5470-106">V2VM</span></span>
```
Register-AzureRmBackupContainer -Name <String> -ResourceGroupName <String> [-Vault] <AzureRMBackupVault>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c5470-107">Opis</span><span class="sxs-lookup"><span data-stu-id="c5470-107">DESCRIPTION</span></span>
<span data-ttu-id="c5470-108">Polecenie cmdlet **register-AzureRmBackupContainer** rejestruje kontener w magazynie kopii zapasowych platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="c5470-108">The **Register-AzureRmBackupContainer** cmdlet registers the container with an Azure Backup vault.</span></span>
<span data-ttu-id="c5470-109">Aby skonfigurować kopię zapasową przy użyciu usługi Kopia zapasowa Azure, najpierw zarejestruj serwer lub maszynę wirtualną w magazynie kopii zapasowych.</span><span class="sxs-lookup"><span data-stu-id="c5470-109">To configure backup by using Azure Backup, first register your server or virtual machine with a Backup vault.</span></span>
<span data-ttu-id="c5470-110">To polecenie cmdlet rejestruje infrastrukturę jako maszynę wirtualną usługi (IaaS) z określonym magazynem.</span><span class="sxs-lookup"><span data-stu-id="c5470-110">This cmdlet registers an infrastructure as a service (IaaS) virtual machine with the specified vault.</span></span>
<span data-ttu-id="c5470-111">Operacja Register kojarzy maszynę wirtualną platformy Azure z magazynem kopii zapasowych i śledzi maszynę wirtualną przez cykl życia kopii zapasowej.</span><span class="sxs-lookup"><span data-stu-id="c5470-111">The register operation associates the Azure virtual machine with the backup vault and tracks the virtual machine through the backup life cycle.</span></span>

## <span data-ttu-id="c5470-112">Przykłady</span><span class="sxs-lookup"><span data-stu-id="c5470-112">EXAMPLES</span></span>

### <span data-ttu-id="c5470-113">Przykład 1: rejestrowanie maszyny wirtualnej w magazynie kopii zapasowych</span><span class="sxs-lookup"><span data-stu-id="c5470-113">Example 1: Register a virtual machine to a Backup vault</span></span>
```
PS C:\>$Vault = Get-AzureRmBackupVault -Name "Vault03"
PS C:\> Register-AzureRmBackupContainer -Vault $Vault -Name "Contoso03Vm" -ServiceName "ContosoService27"
```

<span data-ttu-id="c5470-114">Pierwsze polecenie uzyskuje magazyn o nazwie Vault03 przy użyciu polecenia cmdlet Get-AzureRmBackupVault.</span><span class="sxs-lookup"><span data-stu-id="c5470-114">The first command gets the vault named Vault03 by using the Get-AzureRmBackupVault cmdlet.</span></span>
<span data-ttu-id="c5470-115">Polecenie zapisuje magazyn w zmiennej $Vault.</span><span class="sxs-lookup"><span data-stu-id="c5470-115">The command stores the vault in the $Vault variable.</span></span>

<span data-ttu-id="c5470-116">Drugie polecenie rejestruje maszynę wirtualną o nazwie Contoso03Vm z magazynem w $Vault.</span><span class="sxs-lookup"><span data-stu-id="c5470-116">The second command registers the virtual machine named Contoso03Vm with the vault in $Vault.</span></span>
<span data-ttu-id="c5470-117">Ta maszyna wirtualna należy do usługi o nazwie ContosoService27.</span><span class="sxs-lookup"><span data-stu-id="c5470-117">That virtual machine belongs to the service named ContosoService27.</span></span>

## <span data-ttu-id="c5470-118">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="c5470-118">PARAMETERS</span></span>

### <span data-ttu-id="c5470-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c5470-119">-DefaultProfile</span></span>
<span data-ttu-id="c5470-120">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="c5470-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c5470-121">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="c5470-121">-Name</span></span>
<span data-ttu-id="c5470-122">Określa nazwę maszyny wirtualnej, którą rejestruje ten aplet polecenia.</span><span class="sxs-lookup"><span data-stu-id="c5470-122">Specifies the name of the virtual machine that this cmdlet registers.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c5470-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c5470-123">-ResourceGroupName</span></span>
<span data-ttu-id="c5470-124">Określa nazwę grupy zasobów maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="c5470-124">Specifies the name of the resource group for the virtual machine.</span></span>

```yaml
Type: String
Parameter Sets: V2VM
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c5470-125">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="c5470-125">-ServiceName</span></span>
<span data-ttu-id="c5470-126">Określa nazwę usługi maszyny wirtualnej, którą to polecenie cmdlet rejestruje.</span><span class="sxs-lookup"><span data-stu-id="c5470-126">Specifies the service name of the virtual machine that this cmdlet registers.</span></span>

<span data-ttu-id="c5470-127">Zazwyczaj nazwa usługi w chmurze zawiera sufiks. cloudapp.net.</span><span class="sxs-lookup"><span data-stu-id="c5470-127">Typically, a cloud service name has a suffix .cloudapp.net.</span></span>
<span data-ttu-id="c5470-128">Nie dodawaj sufiksu podczas określania tego parametru.</span><span class="sxs-lookup"><span data-stu-id="c5470-128">Do not include the suffix when you specify this parameter.</span></span>

<span data-ttu-id="c5470-129">Aby uzyskać informacje o maszynie wirtualnej, użyj polecenia cmdlet Get-AzureRMVM.</span><span class="sxs-lookup"><span data-stu-id="c5470-129">To obtain information about a virtual machine, use the Get-AzureRMVM cmdlet.</span></span>
<span data-ttu-id="c5470-130">Nazwa usługi jest właściwością **deploymentname** obiektu maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="c5470-130">The service name is the **DeploymentName** property of the virtual machine object.</span></span>

```yaml
Type: String
Parameter Sets: V1VM
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c5470-131">-Magazyn</span><span class="sxs-lookup"><span data-stu-id="c5470-131">-Vault</span></span>
<span data-ttu-id="c5470-132">Określa magazyn kopii zapasowych, z którym to polecenie cmdlet rejestruje maszynę wirtualną.</span><span class="sxs-lookup"><span data-stu-id="c5470-132">Specifies the Backup vault to which this cmdlet registers virtual machine.</span></span>
<span data-ttu-id="c5470-133">Aby uzyskać obiekt **AzureRmBackupVault** , użyj polecenia cmdlet Get-AzureRmBackupVault.</span><span class="sxs-lookup"><span data-stu-id="c5470-133">To obtain an **AzureRmBackupVault** object, use the Get-AzureRmBackupVault cmdlet.</span></span>

```yaml
Type: AzureRMBackupVault
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c5470-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c5470-134">CommonParameters</span></span>
<span data-ttu-id="c5470-135">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c5470-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c5470-136">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c5470-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c5470-137">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="c5470-137">INPUTS</span></span>

### <span data-ttu-id="c5470-138">AzureRmBackupVault</span><span class="sxs-lookup"><span data-stu-id="c5470-138">AzureRmBackupVault</span></span>

## <span data-ttu-id="c5470-139">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="c5470-139">OUTPUTS</span></span>

### <span data-ttu-id="c5470-140">AzureRmBackupJob</span><span class="sxs-lookup"><span data-stu-id="c5470-140">AzureRmBackupJob</span></span>

## <span data-ttu-id="c5470-141">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="c5470-141">NOTES</span></span>

## <span data-ttu-id="c5470-142">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="c5470-142">RELATED LINKS</span></span>

[<span data-ttu-id="c5470-143">Get-AzureRmBackupVault</span><span class="sxs-lookup"><span data-stu-id="c5470-143">Get-AzureRmBackupVault</span></span>](./Get-AzureRmBackupVault.md)


