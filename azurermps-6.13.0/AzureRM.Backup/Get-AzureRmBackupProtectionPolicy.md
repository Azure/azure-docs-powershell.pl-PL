---
external help file: Microsoft.Azure.Commands.AzureBackup.dll-Help.xml
Module Name: AzureRM.Backup
ms.assetid: B3B708C5-776E-4F1C-BA0B-492CD9057794
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.backup/get-azurermbackupprotectionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Get-AzureRmBackupProtectionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Get-AzureRmBackupProtectionPolicy.md
ms.openlocfilehash: e3e4858e3cb4f3c54c502ac14fb2c5d8e3ba0c63
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93524605"
---
# <span data-ttu-id="fae48-101">Get-AzureRmBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="fae48-101">Get-AzureRmBackupProtectionPolicy</span></span>

## <span data-ttu-id="fae48-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="fae48-102">SYNOPSIS</span></span>
<span data-ttu-id="fae48-103">Pobiera zasady tworzenia kopii zapasowych dla magazynu kopii zapasowych.</span><span class="sxs-lookup"><span data-stu-id="fae48-103">Gets backup policies for a Backup vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fae48-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="fae48-104">SYNTAX</span></span>

```
Get-AzureRmBackupProtectionPolicy [[-Name] <String>] [-Vault] <AzureRMBackupVault>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fae48-105">Opis</span><span class="sxs-lookup"><span data-stu-id="fae48-105">DESCRIPTION</span></span>
<span data-ttu-id="fae48-106">Polecenie cmdlet **Get-AzureRmBackupProtectionPolicy** pobiera zasady tworzenia kopii zapasowych magazynu kopii zapasowych platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="fae48-106">The **Get-AzureRmBackupProtectionPolicy** cmdlet gets backup policies for an Azure Backup vault.</span></span>

## <span data-ttu-id="fae48-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="fae48-107">EXAMPLES</span></span>

### <span data-ttu-id="fae48-108">Przykład 1: wyświetlanie zasad w magazynie</span><span class="sxs-lookup"><span data-stu-id="fae48-108">Example 1: View the policies in a vault</span></span>
```
PS C:\>$Vault = Get-AzureRmBackupVault -Name "Vault03"
PS C:\> Get-AzureRmBackupProtectionPolicy -Vault $Vault 
Name                      Type               ScheduleType       BackupTime
----                      ----               ------------       ----------
contoso01                 AzureVM            Daily              26-Aug-15 3:00:00 PM
DailyBkp                  AzureVM            Daily              26-Aug-15 3:00:00 PM
DefaultPolicy             AzureVM            Daily              26-Aug-15 12:30:00 AM
WeeklyBkp                 AzureVM            Weekly             26-Aug-15 5:00:00 PM
contoso02                 AzureVM            Daily              26-Aug-15 3:00:00 PM
```

<span data-ttu-id="fae48-109">Pierwsze polecenie uzyskuje magazyn o nazwie Vault03 przy użyciu polecenia cmdlet **Get-AzureRmBackupVault** .</span><span class="sxs-lookup"><span data-stu-id="fae48-109">The first command gets the vault named Vault03 by using the **Get-AzureRmBackupVault** cmdlet.</span></span>
<span data-ttu-id="fae48-110">Polecenie zapisuje ten obiekt w zmiennej $Vault.</span><span class="sxs-lookup"><span data-stu-id="fae48-110">The command stores that object in the $Vault variable.</span></span>
<span data-ttu-id="fae48-111">Drugie polecenie pobiera wszystkie zasady ochrony kopii zapasowych dla magazynu w $Vault.</span><span class="sxs-lookup"><span data-stu-id="fae48-111">The second command gets all the Backup protection policies for the vault in $Vault.</span></span>

### <span data-ttu-id="fae48-112">Przykład 2: uzyskiwanie określonych zasad z magazynu</span><span class="sxs-lookup"><span data-stu-id="fae48-112">Example 2: Get a specific policy from a vault</span></span>
```
PS C:\>$Vault = Get-AzureRmBackupVault -Name "Vault03"
PS C:\> Get-AzureRmBackupProtectionPolicy -Vault $Vault -Name "DefaultPolicy"
Name                      Type               ScheduleType       BackupTime
----                      ----               ------------       ----------
DefaultPolicy             AzureVM            Daily              26-Aug-15 12:30:00 AM
```

<span data-ttu-id="fae48-113">Pierwsze polecenie uzyskuje magazyn o nazwie Vault03 przy użyciu polecenia cmdlet **Get-AzureRmBackupVault** .</span><span class="sxs-lookup"><span data-stu-id="fae48-113">The first command gets the vault named Vault03 by using the **Get-AzureRmBackupVault** cmdlet.</span></span>
<span data-ttu-id="fae48-114">Polecenie zapisuje ten obiekt w zmiennej $Vault.</span><span class="sxs-lookup"><span data-stu-id="fae48-114">The command stores that object in the $Vault variable.</span></span>
<span data-ttu-id="fae48-115">Drugie polecenie pobiera zasady ochrony kopii zapasowej o nazwie DefaultPolicy dla magazynu w $Vault.</span><span class="sxs-lookup"><span data-stu-id="fae48-115">The second command gets the Backup protection policy named DefaultPolicy for the vault in $Vault.</span></span>

## <span data-ttu-id="fae48-116">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="fae48-116">PARAMETERS</span></span>

### <span data-ttu-id="fae48-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fae48-117">-DefaultProfile</span></span>
<span data-ttu-id="fae48-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="fae48-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="fae48-119">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="fae48-119">-Name</span></span>
<span data-ttu-id="fae48-120">Określa nazwę zasad, które ma być pobierane przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fae48-120">Specifies the name of the policy that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fae48-121">-Magazyn</span><span class="sxs-lookup"><span data-stu-id="fae48-121">-Vault</span></span>
<span data-ttu-id="fae48-122">Określa magazyn kopii zapasowych, dla którego to polecenie cmdlet pobiera zasady.</span><span class="sxs-lookup"><span data-stu-id="fae48-122">Specifies the Backup vault for which this cmdlet gets policies.</span></span>
<span data-ttu-id="fae48-123">Aby uzyskać obiekt **AzureRmBackupVault** , użyj polecenia cmdlet Get-AzureRmBackupVault.</span><span class="sxs-lookup"><span data-stu-id="fae48-123">To obtain an **AzureRmBackupVault** object, use the Get-AzureRmBackupVault cmdlet.</span></span>

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

### <span data-ttu-id="fae48-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fae48-124">CommonParameters</span></span>
<span data-ttu-id="fae48-125">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fae48-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fae48-126">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fae48-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fae48-127">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="fae48-127">INPUTS</span></span>

### <span data-ttu-id="fae48-128">Microsoft. Azure. Commands. AzureBackup. models. AzureRMBackupVault</span><span class="sxs-lookup"><span data-stu-id="fae48-128">Microsoft.Azure.Commands.AzureBackup.Models.AzureRMBackupVault</span></span>
<span data-ttu-id="fae48-129">Parametry: Magazyn (ByValue)</span><span class="sxs-lookup"><span data-stu-id="fae48-129">Parameters: Vault (ByValue)</span></span>

## <span data-ttu-id="fae48-130">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="fae48-130">OUTPUTS</span></span>

### <span data-ttu-id="fae48-131">Microsoft. Azure. Commands. AzureBackup. models. AzureRMBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="fae48-131">Microsoft.Azure.Commands.AzureBackup.Models.AzureRMBackupProtectionPolicy</span></span>

## <span data-ttu-id="fae48-132">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="fae48-132">NOTES</span></span>

## <span data-ttu-id="fae48-133">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="fae48-133">RELATED LINKS</span></span>

[<span data-ttu-id="fae48-134">Get-AzureRmBackupVault</span><span class="sxs-lookup"><span data-stu-id="fae48-134">Get-AzureRmBackupVault</span></span>](./Get-AzureRmBackupVault.md)

[<span data-ttu-id="fae48-135">Enable-AzureRmBackupProtection</span><span class="sxs-lookup"><span data-stu-id="fae48-135">Enable-AzureRmBackupProtection</span></span>](./Enable-AzureRmBackupProtection.md)

[<span data-ttu-id="fae48-136">Nowe — AzureRmBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="fae48-136">New-AzureRmBackupProtectionPolicy</span></span>](./New-AzureRmBackupProtectionPolicy.md)

[<span data-ttu-id="fae48-137">Remove-AzureRmBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="fae48-137">Remove-AzureRmBackupProtectionPolicy</span></span>](./Remove-AzureRmBackupProtectionPolicy.md)

