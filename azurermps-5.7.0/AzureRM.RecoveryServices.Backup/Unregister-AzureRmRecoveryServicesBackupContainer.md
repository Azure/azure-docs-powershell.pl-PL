---
external help file: Microsoft.Azure.Commands.RecoveryServices.Backup.dll-Help.xml
Module Name: AzureRM.RecoveryServices.Backup
ms.assetid: A10DC2A2-A732-416F-9C68-6533C143AE8F
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.backup/unregister-azurermrecoveryservicesbackupcontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.Backup/Commands.RecoveryServices.Backup/help/Unregister-AzureRmRecoveryServicesBackupContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.Backup/Commands.RecoveryServices.Backup/help/Unregister-AzureRmRecoveryServicesBackupContainer.md
ms.openlocfilehash: 6ad62049600f1734beabcc1a322086aad1a92348
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93548055"
---
# <span data-ttu-id="5ee83-101">Unregister-AzureRmRecoveryServicesBackupContainer</span><span class="sxs-lookup"><span data-stu-id="5ee83-101">Unregister-AzureRmRecoveryServicesBackupContainer</span></span>

## <span data-ttu-id="5ee83-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="5ee83-102">SYNOPSIS</span></span>
<span data-ttu-id="5ee83-103">Wyrejestrowuje serwer z systemem Windows lub inny kontener z magazynu.</span><span class="sxs-lookup"><span data-stu-id="5ee83-103">Unregisters a Windows Server or other container from the vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5ee83-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="5ee83-104">SYNTAX</span></span>

```
Unregister-AzureRmRecoveryServicesBackupContainer [-Container] <ContainerBase> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5ee83-105">Opis</span><span class="sxs-lookup"><span data-stu-id="5ee83-105">DESCRIPTION</span></span>
<span data-ttu-id="5ee83-106">Polecenie cmdlet **Wyrejestrowanie — AzureRmRecoveryServicesBackupContainer** wyrejestruje system Windows Server lub inny kontener kopii zapasowych z magazynu.</span><span class="sxs-lookup"><span data-stu-id="5ee83-106">The **Unregister-AzureRmRecoveryServicesBackupContainer** cmdlet unregisters a Windows Server or other Backup container from the vault.</span></span>
<span data-ttu-id="5ee83-107">To polecenie cmdlet usuwa odwołania do kontenera z magazynu.</span><span class="sxs-lookup"><span data-stu-id="5ee83-107">This cmdlet removes references to a container from the vault.</span></span>
<span data-ttu-id="5ee83-108">Przed wyrejestrowaniem kontenera musisz usunąć wszelkie chronione dane skojarzone z tym kontenerem.</span><span class="sxs-lookup"><span data-stu-id="5ee83-108">Before you can unregister a container, you must delete any protected data associated with that container.</span></span>

<span data-ttu-id="5ee83-109">Przed użyciem bieżącego polecenia cmdlet Ustaw kontekst magazynu przy użyciu polecenia cmdlet Set-AzureRmRecoveryServicesVaultContext.</span><span class="sxs-lookup"><span data-stu-id="5ee83-109">Set the vault context by using the Set-AzureRmRecoveryServicesVaultContext cmdlet before you use the current cmdlet.</span></span>

## <span data-ttu-id="5ee83-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="5ee83-110">EXAMPLES</span></span>

### <span data-ttu-id="5ee83-111">Przykład 1: Wyrejestrowanie serwera Windows z magazynu</span><span class="sxs-lookup"><span data-stu-id="5ee83-111">Example 1: Unregister a Windows Server from the vault</span></span>
```
PS C:\>$Cont = Get-AzureRmRecoveryServicesContainer -ContainerType "Windows" -BackupManagementType MARS -Name "server01.contoso.com"
PS C:\> Unregister-AzureRmRecoveryServicesBackupContainer -Container $Cont
```

<span data-ttu-id="5ee83-112">Pierwsze polecenie uzyskuje kontener systemu Windows o nazwie server01.contoso.com zarejestrowany w magazynie, a następnie zapisuje go w zmiennej $Cont.</span><span class="sxs-lookup"><span data-stu-id="5ee83-112">The first command gets the Windows container named server01.contoso.com that is registered in the vault, and then stores it in the $Cont variable.</span></span>

<span data-ttu-id="5ee83-113">Drugie polecenie wyrejestrowuje określony serwer z magazynu kopii zapasowych platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="5ee83-113">The second command unregisters the specified Windows Server from the Azure Backup vault.</span></span>

## <span data-ttu-id="5ee83-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="5ee83-114">PARAMETERS</span></span>

### <span data-ttu-id="5ee83-115">-Kontener</span><span class="sxs-lookup"><span data-stu-id="5ee83-115">-Container</span></span>
<span data-ttu-id="5ee83-116">Określa obiekt kontenera kopii zapasowych do wyrejestrowania.</span><span class="sxs-lookup"><span data-stu-id="5ee83-116">Specifies a Backup container object to unregister.</span></span>
<span data-ttu-id="5ee83-117">Aby uzyskać obiekt **BackupContainer** , użyj polecenia cmdlet Get-AzureRmRecoveryServicesBackupContainer.</span><span class="sxs-lookup"><span data-stu-id="5ee83-117">To obtain a **BackupContainer** object, use the Get-AzureRmRecoveryServicesBackupContainer cmdlet.</span></span>

```yaml
Type: ContainerBase
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5ee83-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5ee83-118">-DefaultProfile</span></span>
<span data-ttu-id="5ee83-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="5ee83-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5ee83-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="5ee83-120">-PassThru</span></span>
<span data-ttu-id="5ee83-121">Zwraca kontener, który ma zostać usunięty.</span><span class="sxs-lookup"><span data-stu-id="5ee83-121">Return the container to be deleted.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5ee83-122">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="5ee83-122">-Confirm</span></span>
<span data-ttu-id="5ee83-123">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5ee83-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5ee83-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5ee83-124">-WhatIf</span></span>
<span data-ttu-id="5ee83-125">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5ee83-125">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="5ee83-126">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="5ee83-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5ee83-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5ee83-127">CommonParameters</span></span>
<span data-ttu-id="5ee83-128">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5ee83-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5ee83-129">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5ee83-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5ee83-130">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="5ee83-130">INPUTS</span></span>

### <span data-ttu-id="5ee83-131">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="5ee83-131">None</span></span>
<span data-ttu-id="5ee83-132">To polecenie cmdlet nie akceptuje żadnych danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="5ee83-132">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="5ee83-133">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="5ee83-133">OUTPUTS</span></span>

## <span data-ttu-id="5ee83-134">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="5ee83-134">NOTES</span></span>

## <span data-ttu-id="5ee83-135">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="5ee83-135">RELATED LINKS</span></span>

[<span data-ttu-id="5ee83-136">Get-AzureRmRecoveryServicesBackupContainer</span><span class="sxs-lookup"><span data-stu-id="5ee83-136">Get-AzureRmRecoveryServicesBackupContainer</span></span>](./Get-AzureRmRecoveryServicesBackupContainer.md)


