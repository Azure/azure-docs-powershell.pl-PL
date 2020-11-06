---
external help file: Microsoft.Azure.Commands.RecoveryServices.ARM.dll-Help.xml
Module Name: AzureRM.RecoveryServices
ms.assetid: 9591E150-54DA-48B7-8656-3891833FE61E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices/new-azurermrecoveryservicesvault
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices/help/New-AzureRmRecoveryServicesVault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices/help/New-AzureRmRecoveryServicesVault.md
ms.openlocfilehash: 3abb13803dbe564eb7562691b10a453174374444
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93550591"
---
# <span data-ttu-id="66130-101">New-AzureRmRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="66130-101">New-AzureRmRecoveryServicesVault</span></span>

## <span data-ttu-id="66130-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="66130-102">SYNOPSIS</span></span>
<span data-ttu-id="66130-103">Tworzy nowy magazyn usług Recovery Services.</span><span class="sxs-lookup"><span data-stu-id="66130-103">Creates a new Recovery Services vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="66130-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="66130-104">SYNTAX</span></span>

```
New-AzureRmRecoveryServicesVault -Name <String> -ResourceGroupName <String> -Location <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="66130-105">Opis</span><span class="sxs-lookup"><span data-stu-id="66130-105">DESCRIPTION</span></span>
<span data-ttu-id="66130-106">Polecenie cmdlet **New-AzureRmRecoveryServicesVault** tworzy nowy magazyn usług Recovery Services.</span><span class="sxs-lookup"><span data-stu-id="66130-106">The **New-AzureRmRecoveryServicesVault** cmdlet creates a new Recovery Services vault.</span></span>

## <span data-ttu-id="66130-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="66130-107">EXAMPLES</span></span>

### <span data-ttu-id="66130-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="66130-108">Example 1</span></span>
```
PS C:\> New-AzureRmRecoveryServicesVault -Name "vaultName" -ResourceGroupName "rg" -Location "eastasia"
```

<span data-ttu-id="66130-109">Utwórz magazyn usługi odzyskiwania w grupie zasobów i podanej lokalizacji.</span><span class="sxs-lookup"><span data-stu-id="66130-109">Create recovery service vault in resource group and given location.</span></span>

## <span data-ttu-id="66130-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="66130-110">PARAMETERS</span></span>

### <span data-ttu-id="66130-111">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="66130-111">-Location</span></span>
<span data-ttu-id="66130-112">Określa nazwę lokalizacji geograficznej magazynu.</span><span class="sxs-lookup"><span data-stu-id="66130-112">Specifies the name of the geographic location of the vault.</span></span>

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

### <span data-ttu-id="66130-113">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="66130-113">-Name</span></span>
<span data-ttu-id="66130-114">Określa nazwę magazynu, który ma zostać utworzony.</span><span class="sxs-lookup"><span data-stu-id="66130-114">Specifies the name of the vault to create.</span></span>

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

### <span data-ttu-id="66130-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="66130-115">-ResourceGroupName</span></span>
<span data-ttu-id="66130-116">Określa nazwę grupy zasobów platformy Azure, w której należy utworzyć lub z której ma zostać pobrany określony obiekt usług Recovery Services.</span><span class="sxs-lookup"><span data-stu-id="66130-116">Specifies the name of the Azure resource group in which to create or from which to retrieve the specified Recovery Services object.</span></span>

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

### <span data-ttu-id="66130-117">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="66130-117">-Confirm</span></span>
<span data-ttu-id="66130-118">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="66130-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="66130-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="66130-119">-WhatIf</span></span>
<span data-ttu-id="66130-120">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="66130-120">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="66130-121">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="66130-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="66130-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="66130-122">-DefaultProfile</span></span>
<span data-ttu-id="66130-123">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="66130-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="66130-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="66130-124">CommonParameters</span></span>
<span data-ttu-id="66130-125">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="66130-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="66130-126">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="66130-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="66130-127">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="66130-127">INPUTS</span></span>

### <span data-ttu-id="66130-128">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="66130-128">None</span></span>
<span data-ttu-id="66130-129">To polecenie cmdlet nie akceptuje żadnych danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="66130-129">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="66130-130">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="66130-130">OUTPUTS</span></span>

### <span data-ttu-id="66130-131">Microsoft. Azure. Commands. RecoveryServices. ARSVault</span><span class="sxs-lookup"><span data-stu-id="66130-131">Microsoft.Azure.Commands.RecoveryServices.ARSVault</span></span>

## <span data-ttu-id="66130-132">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="66130-132">NOTES</span></span>

## <span data-ttu-id="66130-133">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="66130-133">RELATED LINKS</span></span>

[<span data-ttu-id="66130-134">Get-AzureRmRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="66130-134">Get-AzureRmRecoveryServicesVault</span></span>](./Get-AzureRmRecoveryServicesVault.md)

[<span data-ttu-id="66130-135">Get-AzureRmRecoveryServicesVaultSettingsFile</span><span class="sxs-lookup"><span data-stu-id="66130-135">Get-AzureRmRecoveryServicesVaultSettingsFile</span></span>](./Get-AzureRmRecoveryServicesVaultSettingsFile.md)

[<span data-ttu-id="66130-136">Remove-AzureRmRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="66130-136">Remove-AzureRmRecoveryServicesVault</span></span>](./Remove-AzureRmRecoveryServicesVault.md)


