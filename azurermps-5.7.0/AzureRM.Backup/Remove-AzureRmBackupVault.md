---
external help file: Microsoft.Azure.Commands.AzureBackup.dll-Help.xml
Module Name: AzureRM.Backup
ms.assetid: 698DCD00-13C0-4C36-A74B-35215D608339
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.backup/remove-azurermbackupvault
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Remove-AzureRmBackupVault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Remove-AzureRmBackupVault.md
ms.openlocfilehash: 4b8098889cbec7bd313ffb2ed70c5384a7e24ef0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93550699"
---
# <span data-ttu-id="976b5-101">Remove-AzureRmBackupVault</span><span class="sxs-lookup"><span data-stu-id="976b5-101">Remove-AzureRmBackupVault</span></span>

## <span data-ttu-id="976b5-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="976b5-102">SYNOPSIS</span></span>
<span data-ttu-id="976b5-103">Usuwa magazyn kopii zapasowych.</span><span class="sxs-lookup"><span data-stu-id="976b5-103">Deletes a Backup vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="976b5-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="976b5-104">SYNTAX</span></span>

```
Remove-AzureRmBackupVault [-Force] [-Vault] <AzureRMBackupVault> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="976b5-105">Opis</span><span class="sxs-lookup"><span data-stu-id="976b5-105">DESCRIPTION</span></span>
<span data-ttu-id="976b5-106">Polecenie cmdlet **Remove-AzureRmBackupVault** usuwa magazyn kopii zapasowych platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="976b5-106">The **Remove-AzureRmBackupVault** cmdlet deletes an Azure Backup vault.</span></span>

<span data-ttu-id="976b5-107">Aby można było usunąć magazyn kopii zapasowych, musi on być pusty.</span><span class="sxs-lookup"><span data-stu-id="976b5-107">Before you can delete a Backup vault, it must be empty.</span></span>
<span data-ttu-id="976b5-108">Użyj polecenia cmdlet **Remove-AzureRmBackupContainer** w celu usunięcia infrastruktury jako danych kopii zapasowej maszyny wirtualnej usługi (IaaS) z magazynu.</span><span class="sxs-lookup"><span data-stu-id="976b5-108">Use the **Remove-AzureRmBackupContainer** cmdlet to remove infrastructure as a service (IaaS) virtual machine backup data from the vault.</span></span>
<span data-ttu-id="976b5-109">Użyj polecenia cmdlet **delete-RegisteredServer** , aby usunąć inne zarejestrowane serwery i dane kopii zapasowej.</span><span class="sxs-lookup"><span data-stu-id="976b5-109">Use the **Delete-RegisteredServer** cmdlet to remove other registered servers and backup data.</span></span>

## <span data-ttu-id="976b5-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="976b5-110">EXAMPLES</span></span>

### <span data-ttu-id="976b5-111">Przykład 1: Usuwanie magazynu kopii zapasowych Azure</span><span class="sxs-lookup"><span data-stu-id="976b5-111">Example 1: Delete an Azure Backup vault</span></span>
```
PS C:\>Get-AzureRmBackupVault -Name "Vault03" | Remove-AzureRmBackupVault
```

<span data-ttu-id="976b5-112">To polecenie pobiera magazyn kopii zapasowych Azure o nazwie Vault03 przy użyciu polecenia cmdlet **Get-AzureRmBackupVault** .</span><span class="sxs-lookup"><span data-stu-id="976b5-112">This command gets the Azure Backup vault named Vault03 by using the **Get-AzureRmBackupVault** cmdlet.</span></span>
<span data-ttu-id="976b5-113">Polecenie przekazuje ten magazyn do bieżącego polecenia cmdlet za pomocą operatora potoku.</span><span class="sxs-lookup"><span data-stu-id="976b5-113">The command passes that vault to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="976b5-114">Bieżące polecenie cmdlet usuwa magazyn.</span><span class="sxs-lookup"><span data-stu-id="976b5-114">The current cmdlet removes the vault.</span></span>

## <span data-ttu-id="976b5-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="976b5-115">PARAMETERS</span></span>

### <span data-ttu-id="976b5-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="976b5-116">-DefaultProfile</span></span>
<span data-ttu-id="976b5-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="976b5-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="976b5-118">-Force</span><span class="sxs-lookup"><span data-stu-id="976b5-118">-Force</span></span>
```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="976b5-119">-Magazyn</span><span class="sxs-lookup"><span data-stu-id="976b5-119">-Vault</span></span>
<span data-ttu-id="976b5-120">Określa magazyn kopii zapasowych, który jest usuwany przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="976b5-120">Specifies a Backup vault that this cmdlet removes.</span></span>
<span data-ttu-id="976b5-121">Aby uzyskać **AzureRmBackupVault** , użyj polecenia cmdlet Get-AzureRmBackupVault.</span><span class="sxs-lookup"><span data-stu-id="976b5-121">To obtain an **AzureRmBackupVault** , use the Get-AzureRmBackupVault cmdlet.</span></span>

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

### <span data-ttu-id="976b5-122">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="976b5-122">-Confirm</span></span>
<span data-ttu-id="976b5-123">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="976b5-123">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="976b5-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="976b5-124">-WhatIf</span></span>
<span data-ttu-id="976b5-125">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="976b5-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="976b5-126">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="976b5-126">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="976b5-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="976b5-127">CommonParameters</span></span>
<span data-ttu-id="976b5-128">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="976b5-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="976b5-129">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="976b5-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="976b5-130">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="976b5-130">INPUTS</span></span>

### <span data-ttu-id="976b5-131">AzureRMBackupVault</span><span class="sxs-lookup"><span data-stu-id="976b5-131">AzureRMBackupVault</span></span>

## <span data-ttu-id="976b5-132">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="976b5-132">OUTPUTS</span></span>

### <span data-ttu-id="976b5-133">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="976b5-133">None</span></span>

## <span data-ttu-id="976b5-134">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="976b5-134">NOTES</span></span>
* <span data-ttu-id="976b5-135">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="976b5-135">None</span></span>

## <span data-ttu-id="976b5-136">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="976b5-136">RELATED LINKS</span></span>

[<span data-ttu-id="976b5-137">Get-AzureRmBackupVault</span><span class="sxs-lookup"><span data-stu-id="976b5-137">Get-AzureRmBackupVault</span></span>](./Get-AzureRmBackupVault.md)

[<span data-ttu-id="976b5-138">Nowe — AzureRmBackupVault</span><span class="sxs-lookup"><span data-stu-id="976b5-138">New-AzureRmBackupVault</span></span>](./New-AzureRmBackupVault.md)

[<span data-ttu-id="976b5-139">Set-AzureRmBackupVault</span><span class="sxs-lookup"><span data-stu-id="976b5-139">Set-AzureRmBackupVault</span></span>](./Set-AzureRmBackupVault.md)


