---
external help file: Microsoft.Azure.Commands.RecoveryServices.ARM.dll-Help.xml
Module Name: AzureRM.RecoveryServices
ms.assetid: C635D723-0F03-4EF8-9435-24DBE0859899
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices/set-azurermrecoveryservicesbackupproperties
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices/help/Set-AzureRmRecoveryServicesBackupProperties.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices/help/Set-AzureRmRecoveryServicesBackupProperties.md
ms.openlocfilehash: d8512567a7dd094f14c4bb49a7f575dd13341d10
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93549596"
---
# <span data-ttu-id="10e87-101">Set-AzureRmRecoveryServicesBackupProperties</span><span class="sxs-lookup"><span data-stu-id="10e87-101">Set-AzureRmRecoveryServicesBackupProperties</span></span>

## <span data-ttu-id="10e87-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="10e87-102">SYNOPSIS</span></span>
<span data-ttu-id="10e87-103">Ustawia właściwości zarządzania kopią zapasową.</span><span class="sxs-lookup"><span data-stu-id="10e87-103">Sets the properties for backup management.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="10e87-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="10e87-104">SYNTAX</span></span>

```
Set-AzureRmRecoveryServicesBackupProperties -Vault <ARSVault>
 [-BackupStorageRedundancy <AzureRmRecoveryServicesBackupStorageRedundancyType>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="10e87-105">Opis</span><span class="sxs-lookup"><span data-stu-id="10e87-105">DESCRIPTION</span></span>
<span data-ttu-id="10e87-106">Polecenie cmdlet **Set-AzureRmRecoveryServicesBackupProperties** ustawia właściwości magazynu kopii zapasowej dla magazynu usług odzyskiwania.</span><span class="sxs-lookup"><span data-stu-id="10e87-106">The **Set-AzureRmRecoveryServicesBackupProperties** cmdlet sets backup storage properties for a Recovery Services vault.</span></span>

## <span data-ttu-id="10e87-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="10e87-107">EXAMPLES</span></span>

### <span data-ttu-id="10e87-108">Przykład 1: Ustawianie magazynu geonadmiarowości w magazynie</span><span class="sxs-lookup"><span data-stu-id="10e87-108">Example 1: Set GeoRedundant storage for a vault</span></span>
```
PS C:\> $Vault01 = Get-AzureRmRecoveryServicesVault -Name "TestVault"
PS C:\> Set-AzureRmRecoveryServicesBackupProperties -Vault $Vault01 -BackupStorageRedundancy GeoRedundant
```

<span data-ttu-id="10e87-109">Pierwsze polecenie uzyskuje magazyn o nazwie TestVault, a następnie zapisuje go w zmiennej $Vault 01.</span><span class="sxs-lookup"><span data-stu-id="10e87-109">The first command gets the vault named TestVault, and then stores it in the $Vault01 variable.</span></span>

<span data-ttu-id="10e87-110">Drugie polecenie ustawia nadmiarowość miejsca do magazynowania kopii zapasowej $Vault 01 do georezerwowania.</span><span class="sxs-lookup"><span data-stu-id="10e87-110">The second command sets the backup storage redundancy for $Vault01 to GeoRedundant.</span></span>

## <span data-ttu-id="10e87-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="10e87-111">PARAMETERS</span></span>

### <span data-ttu-id="10e87-112">-BackupStorageRedundancy</span><span class="sxs-lookup"><span data-stu-id="10e87-112">-BackupStorageRedundancy</span></span>
<span data-ttu-id="10e87-113">Określa typ nadmiarowości miejsca do magazynowania kopii zapasowych.</span><span class="sxs-lookup"><span data-stu-id="10e87-113">Specifies the backup storage redundancy type.</span></span>

```yaml
Type: AzureRmRecoveryServicesBackupStorageRedundancyType
Parameter Sets: (All)
Aliases: 
Accepted values: GeoRedundant, LocallyRedundant

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="10e87-114">-Magazyn</span><span class="sxs-lookup"><span data-stu-id="10e87-114">-Vault</span></span>
<span data-ttu-id="10e87-115">Określa nazwę magazynu.</span><span class="sxs-lookup"><span data-stu-id="10e87-115">Specifies the name of the vault.</span></span>
<span data-ttu-id="10e87-116">Magazyn musi być obiektem **AzureRmRecoveryServicesVault** .</span><span class="sxs-lookup"><span data-stu-id="10e87-116">The vault must be an **AzureRmRecoveryServicesVault** object.</span></span>

```yaml
Type: ARSVault
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="10e87-117">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="10e87-117">-Confirm</span></span>
<span data-ttu-id="10e87-118">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="10e87-118">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="10e87-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="10e87-119">-WhatIf</span></span>
<span data-ttu-id="10e87-120">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="10e87-120">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="10e87-121">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="10e87-121">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="10e87-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="10e87-122">-DefaultProfile</span></span>
<span data-ttu-id="10e87-123">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="10e87-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="10e87-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="10e87-124">CommonParameters</span></span>
<span data-ttu-id="10e87-125">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="10e87-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="10e87-126">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="10e87-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="10e87-127">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="10e87-127">INPUTS</span></span>

### <span data-ttu-id="10e87-128">ARSVault</span><span class="sxs-lookup"><span data-stu-id="10e87-128">ARSVault</span></span>
<span data-ttu-id="10e87-129">Parametr "magazyn" akceptuje wartość typu "ARSVault" z potoku.</span><span class="sxs-lookup"><span data-stu-id="10e87-129">Parameter 'Vault' accepts value of type 'ARSVault' from the pipeline</span></span>

## <span data-ttu-id="10e87-130">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="10e87-130">OUTPUTS</span></span>

## <span data-ttu-id="10e87-131">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="10e87-131">NOTES</span></span>

## <span data-ttu-id="10e87-132">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="10e87-132">RELATED LINKS</span></span>

[<span data-ttu-id="10e87-133">Get-AzureRmRecoveryServicesBackupProperties</span><span class="sxs-lookup"><span data-stu-id="10e87-133">Get-AzureRmRecoveryServicesBackupProperties</span></span>](./Get-AzureRmRecoveryServicesBackupProperties.md)

[<span data-ttu-id="10e87-134">Get-AzureRmRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="10e87-134">Get-AzureRmRecoveryServicesVault</span></span>](./Get-AzureRmRecoveryServicesVault.md)


