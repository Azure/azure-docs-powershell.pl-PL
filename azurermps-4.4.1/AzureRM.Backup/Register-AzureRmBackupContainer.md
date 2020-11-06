---
external help file: Microsoft.Azure.Commands.AzureBackup.dll-Help.xml
Module Name: AzureRM.Backup
ms.assetid: 394500DB-D2BB-4793-8D9F-2CAF4D892A55
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Register-AzureRmBackupContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Register-AzureRmBackupContainer.md
ms.openlocfilehash: fe1e1075e14e3752024edff1b68db88419d5bcd6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93547083"
---
# <span data-ttu-id="02a0d-101">Register-AzureRmBackupContainer</span><span class="sxs-lookup"><span data-stu-id="02a0d-101">Register-AzureRmBackupContainer</span></span>

## <span data-ttu-id="02a0d-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="02a0d-102">SYNOPSIS</span></span>
<span data-ttu-id="02a0d-103">Rejestruje kontener z magazynem kopii zapasowej.</span><span class="sxs-lookup"><span data-stu-id="02a0d-103">Registers the container with a Backup vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="02a0d-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="02a0d-104">SYNTAX</span></span>

### <span data-ttu-id="02a0d-105">V1VM</span><span class="sxs-lookup"><span data-stu-id="02a0d-105">V1VM</span></span>
```
Register-AzureRmBackupContainer -Name <String> -ServiceName <String> [-Vault] <AzureRMBackupVault>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="02a0d-106">V2VM</span><span class="sxs-lookup"><span data-stu-id="02a0d-106">V2VM</span></span>
```
Register-AzureRmBackupContainer -Name <String> -ResourceGroupName <String> [-Vault] <AzureRMBackupVault>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="02a0d-107">Opis</span><span class="sxs-lookup"><span data-stu-id="02a0d-107">DESCRIPTION</span></span>
<span data-ttu-id="02a0d-108">Polecenie cmdlet **register-AzureRmBackupContainer** rejestruje kontener w magazynie kopii zapasowych platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="02a0d-108">The **Register-AzureRmBackupContainer** cmdlet registers the container with an Azure Backup vault.</span></span>
<span data-ttu-id="02a0d-109">Aby skonfigurować kopię zapasową przy użyciu usługi Kopia zapasowa Azure, najpierw zarejestruj serwer lub maszynę wirtualną w magazynie kopii zapasowych.</span><span class="sxs-lookup"><span data-stu-id="02a0d-109">To configure backup by using Azure Backup, first register your server or virtual machine with a Backup vault.</span></span>
<span data-ttu-id="02a0d-110">To polecenie cmdlet rejestruje infrastrukturę jako maszynę wirtualną usługi (IaaS) z określonym magazynem.</span><span class="sxs-lookup"><span data-stu-id="02a0d-110">This cmdlet registers an infrastructure as a service (IaaS) virtual machine with the specified vault.</span></span>
<span data-ttu-id="02a0d-111">Operacja Register kojarzy maszynę wirtualną platformy Azure z magazynem kopii zapasowych i śledzi maszynę wirtualną przez cykl życia kopii zapasowej.</span><span class="sxs-lookup"><span data-stu-id="02a0d-111">The register operation associates the Azure virtual machine with the backup vault and tracks the virtual machine through the backup life cycle.</span></span>

## <span data-ttu-id="02a0d-112">Przykłady</span><span class="sxs-lookup"><span data-stu-id="02a0d-112">EXAMPLES</span></span>

### <span data-ttu-id="02a0d-113">Przykład 1: rejestrowanie maszyny wirtualnej w magazynie kopii zapasowych</span><span class="sxs-lookup"><span data-stu-id="02a0d-113">Example 1: Register a virtual machine to a Backup vault</span></span>
```
PS C:\>$Vault = Get-AzureRmBackupVault -Name "Vault03"
PS C:\> Register-AzureRmBackupContainer -Vault $Vault -Name "Contoso03Vm" -ServiceName "ContosoService27"
```

<span data-ttu-id="02a0d-114">Pierwsze polecenie uzyskuje magazyn o nazwie Vault03 przy użyciu polecenia cmdlet Get-AzureRmBackupVault.</span><span class="sxs-lookup"><span data-stu-id="02a0d-114">The first command gets the vault named Vault03 by using the Get-AzureRmBackupVault cmdlet.</span></span>
<span data-ttu-id="02a0d-115">Polecenie zapisuje magazyn w zmiennej $Vault.</span><span class="sxs-lookup"><span data-stu-id="02a0d-115">The command stores the vault in the $Vault variable.</span></span>

<span data-ttu-id="02a0d-116">Drugie polecenie rejestruje maszynę wirtualną o nazwie Contoso03Vm z magazynem w $Vault.</span><span class="sxs-lookup"><span data-stu-id="02a0d-116">The second command registers the virtual machine named Contoso03Vm with the vault in $Vault.</span></span>
<span data-ttu-id="02a0d-117">Ta maszyna wirtualna należy do usługi o nazwie ContosoService27.</span><span class="sxs-lookup"><span data-stu-id="02a0d-117">That virtual machine belongs to the service named ContosoService27.</span></span>

## <span data-ttu-id="02a0d-118">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="02a0d-118">PARAMETERS</span></span>

### <span data-ttu-id="02a0d-119">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="02a0d-119">-Name</span></span>
<span data-ttu-id="02a0d-120">Określa nazwę maszyny wirtualnej, którą rejestruje ten aplet polecenia.</span><span class="sxs-lookup"><span data-stu-id="02a0d-120">Specifies the name of the virtual machine that this cmdlet registers.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="02a0d-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="02a0d-121">-ResourceGroupName</span></span>
<span data-ttu-id="02a0d-122">Określa nazwę grupy zasobów maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="02a0d-122">Specifies the name of the resource group for the virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: V2VM
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="02a0d-123">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="02a0d-123">-ServiceName</span></span>
<span data-ttu-id="02a0d-124">Określa nazwę usługi maszyny wirtualnej, którą to polecenie cmdlet rejestruje.</span><span class="sxs-lookup"><span data-stu-id="02a0d-124">Specifies the service name of the virtual machine that this cmdlet registers.</span></span>

<span data-ttu-id="02a0d-125">Zazwyczaj nazwa usługi w chmurze zawiera sufiks. cloudapp.net.</span><span class="sxs-lookup"><span data-stu-id="02a0d-125">Typically, a cloud service name has a suffix .cloudapp.net.</span></span>
<span data-ttu-id="02a0d-126">Nie dodawaj sufiksu podczas określania tego parametru.</span><span class="sxs-lookup"><span data-stu-id="02a0d-126">Do not include the suffix when you specify this parameter.</span></span>

<span data-ttu-id="02a0d-127">Aby uzyskać informacje o maszynie wirtualnej, użyj polecenia cmdlet Get-AzureRMVM.</span><span class="sxs-lookup"><span data-stu-id="02a0d-127">To obtain information about a virtual machine, use the Get-AzureRMVM cmdlet.</span></span>
<span data-ttu-id="02a0d-128">Nazwa usługi jest właściwością **deploymentname** obiektu maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="02a0d-128">The service name is the **DeploymentName** property of the virtual machine object.</span></span>

```yaml
Type: System.String
Parameter Sets: V1VM
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="02a0d-129">-Magazyn</span><span class="sxs-lookup"><span data-stu-id="02a0d-129">-Vault</span></span>
<span data-ttu-id="02a0d-130">Określa magazyn kopii zapasowych, z którym to polecenie cmdlet rejestruje maszynę wirtualną.</span><span class="sxs-lookup"><span data-stu-id="02a0d-130">Specifies the Backup vault to which this cmdlet registers virtual machine.</span></span>
<span data-ttu-id="02a0d-131">Aby uzyskać obiekt **AzureRmBackupVault** , użyj polecenia cmdlet Get-AzureRmBackupVault.</span><span class="sxs-lookup"><span data-stu-id="02a0d-131">To obtain an **AzureRmBackupVault** object, use the Get-AzureRmBackupVault cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.AzureBackup.Models.AzureRMBackupVault
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="02a0d-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="02a0d-132">-DefaultProfile</span></span>
<span data-ttu-id="02a0d-133">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="02a0d-133">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="02a0d-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="02a0d-134">CommonParameters</span></span>
<span data-ttu-id="02a0d-135">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="02a0d-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="02a0d-136">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="02a0d-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="02a0d-137">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="02a0d-137">INPUTS</span></span>

### <span data-ttu-id="02a0d-138">AzureRmBackupVault</span><span class="sxs-lookup"><span data-stu-id="02a0d-138">AzureRmBackupVault</span></span>

## <span data-ttu-id="02a0d-139">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="02a0d-139">OUTPUTS</span></span>

### <span data-ttu-id="02a0d-140">AzureRmBackupJob</span><span class="sxs-lookup"><span data-stu-id="02a0d-140">AzureRmBackupJob</span></span>

## <span data-ttu-id="02a0d-141">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="02a0d-141">NOTES</span></span>

## <span data-ttu-id="02a0d-142">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="02a0d-142">RELATED LINKS</span></span>

[<span data-ttu-id="02a0d-143">Get-AzureRmBackupVault</span><span class="sxs-lookup"><span data-stu-id="02a0d-143">Get-AzureRmBackupVault</span></span>](./Get-AzureRmBackupVault.md)


