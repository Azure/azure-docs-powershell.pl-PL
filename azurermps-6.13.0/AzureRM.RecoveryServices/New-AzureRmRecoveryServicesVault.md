---
external help file: Microsoft.Azure.Commands.RecoveryServices.ARM.dll-Help.xml
Module Name: AzureRM.RecoveryServices
ms.assetid: 9591E150-54DA-48B7-8656-3891833FE61E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices/new-azurermrecoveryservicesvault
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices/help/New-AzureRmRecoveryServicesVault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices/help/New-AzureRmRecoveryServicesVault.md
ms.openlocfilehash: 08166ea1ebe4c78521a68f9e5423a7947e78b699
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93552587"
---
# <span data-ttu-id="5def0-101">New-AzureRmRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="5def0-101">New-AzureRmRecoveryServicesVault</span></span>

## <span data-ttu-id="5def0-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="5def0-102">SYNOPSIS</span></span>
<span data-ttu-id="5def0-103">Tworzy nowy magazyn usług Recovery Services.</span><span class="sxs-lookup"><span data-stu-id="5def0-103">Creates a new Recovery Services vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5def0-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="5def0-104">SYNTAX</span></span>

```
New-AzureRmRecoveryServicesVault -Name <String> -ResourceGroupName <String> -Location <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5def0-105">Opis</span><span class="sxs-lookup"><span data-stu-id="5def0-105">DESCRIPTION</span></span>
<span data-ttu-id="5def0-106">Polecenie cmdlet **New-AzureRmRecoveryServicesVault** tworzy nowy magazyn usług Recovery Services.</span><span class="sxs-lookup"><span data-stu-id="5def0-106">The **New-AzureRmRecoveryServicesVault** cmdlet creates a new Recovery Services vault.</span></span>

## <span data-ttu-id="5def0-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="5def0-107">EXAMPLES</span></span>

### <span data-ttu-id="5def0-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="5def0-108">Example 1</span></span>
```
PS C:\> New-AzureRmRecoveryServicesVault -Name "vaultName" -ResourceGroupName "rg" -Location "eastasia"
```

<span data-ttu-id="5def0-109">Utwórz magazyn usługi odzyskiwania w grupie zasobów i podanej lokalizacji.</span><span class="sxs-lookup"><span data-stu-id="5def0-109">Create recovery service vault in resource group and given location.</span></span>

## <span data-ttu-id="5def0-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="5def0-110">PARAMETERS</span></span>

### <span data-ttu-id="5def0-111">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="5def0-111">-Location</span></span>
<span data-ttu-id="5def0-112">Określa nazwę lokalizacji geograficznej magazynu.</span><span class="sxs-lookup"><span data-stu-id="5def0-112">Specifies the name of the geographic location of the vault.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5def0-113">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="5def0-113">-Name</span></span>
<span data-ttu-id="5def0-114">Określa nazwę magazynu, który ma zostać utworzony.</span><span class="sxs-lookup"><span data-stu-id="5def0-114">Specifies the name of the vault to create.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5def0-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5def0-115">-ResourceGroupName</span></span>
<span data-ttu-id="5def0-116">Określa nazwę grupy zasobów platformy Azure, w której należy utworzyć lub z której ma zostać pobrany określony obiekt usług Recovery Services.</span><span class="sxs-lookup"><span data-stu-id="5def0-116">Specifies the name of the Azure resource group in which to create or from which to retrieve the specified Recovery Services object.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5def0-117">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="5def0-117">-Confirm</span></span>
<span data-ttu-id="5def0-118">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5def0-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5def0-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5def0-119">-WhatIf</span></span>
<span data-ttu-id="5def0-120">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5def0-120">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="5def0-121">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="5def0-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5def0-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5def0-122">-DefaultProfile</span></span>
<span data-ttu-id="5def0-123">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="5def0-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5def0-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5def0-124">CommonParameters</span></span>
<span data-ttu-id="5def0-125">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5def0-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5def0-126">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5def0-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5def0-127">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="5def0-127">INPUTS</span></span>

### <span data-ttu-id="5def0-128">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="5def0-128">None</span></span>

## <span data-ttu-id="5def0-129">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="5def0-129">OUTPUTS</span></span>

### <span data-ttu-id="5def0-130">Microsoft. Azure. Commands. RecoveryServices. ARSVault</span><span class="sxs-lookup"><span data-stu-id="5def0-130">Microsoft.Azure.Commands.RecoveryServices.ARSVault</span></span>

## <span data-ttu-id="5def0-131">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="5def0-131">NOTES</span></span>

## <span data-ttu-id="5def0-132">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="5def0-132">RELATED LINKS</span></span>

[<span data-ttu-id="5def0-133">Get-AzureRmRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="5def0-133">Get-AzureRmRecoveryServicesVault</span></span>](./Get-AzureRmRecoveryServicesVault.md)

[<span data-ttu-id="5def0-134">Get-AzureRmRecoveryServicesVaultSettingsFile</span><span class="sxs-lookup"><span data-stu-id="5def0-134">Get-AzureRmRecoveryServicesVaultSettingsFile</span></span>](./Get-AzureRmRecoveryServicesVaultSettingsFile.md)

[<span data-ttu-id="5def0-135">Remove-AzureRmRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="5def0-135">Remove-AzureRmRecoveryServicesVault</span></span>](./Remove-AzureRmRecoveryServicesVault.md)


