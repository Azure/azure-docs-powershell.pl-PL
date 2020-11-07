---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: 9591E150-54DA-48B7-8656-3891833FE61E
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/new-azrecoveryservicesvault
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/New-AzRecoveryServicesVault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/New-AzRecoveryServicesVault.md
ms.openlocfilehash: 65694116a924759c4cf29a7abcf95da7a03df39f
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93708615"
---
# <span data-ttu-id="da23f-101">New-AzRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="da23f-101">New-AzRecoveryServicesVault</span></span>

## <span data-ttu-id="da23f-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="da23f-102">SYNOPSIS</span></span>
<span data-ttu-id="da23f-103">Tworzy nowy magazyn usług Recovery Services.</span><span class="sxs-lookup"><span data-stu-id="da23f-103">Creates a new Recovery Services vault.</span></span>

## <span data-ttu-id="da23f-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="da23f-104">SYNTAX</span></span>

```
New-AzRecoveryServicesVault -Name <String> -ResourceGroupName <String> -Location <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="da23f-105">Opis</span><span class="sxs-lookup"><span data-stu-id="da23f-105">DESCRIPTION</span></span>
<span data-ttu-id="da23f-106">Polecenie cmdlet **New-AzRecoveryServicesVault** tworzy nowy magazyn usług Recovery Services.</span><span class="sxs-lookup"><span data-stu-id="da23f-106">The **New-AzRecoveryServicesVault** cmdlet creates a new Recovery Services vault.</span></span>

## <span data-ttu-id="da23f-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="da23f-107">EXAMPLES</span></span>

### <span data-ttu-id="da23f-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="da23f-108">Example 1</span></span>
```
PS C:\> New-AzRecoveryServicesVault -Name "vaultName" -ResourceGroupName "rg" -Location "eastasia"
```

<span data-ttu-id="da23f-109">Utwórz magazyn usługi odzyskiwania w grupie zasobów i podanej lokalizacji.</span><span class="sxs-lookup"><span data-stu-id="da23f-109">Create recovery service vault in resource group and given location.</span></span>

## <span data-ttu-id="da23f-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="da23f-110">PARAMETERS</span></span>

### <span data-ttu-id="da23f-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="da23f-111">-DefaultProfile</span></span>
<span data-ttu-id="da23f-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="da23f-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="da23f-113">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="da23f-113">-Location</span></span>
<span data-ttu-id="da23f-114">Określa nazwę lokalizacji geograficznej magazynu.</span><span class="sxs-lookup"><span data-stu-id="da23f-114">Specifies the name of the geographic location of the vault.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="da23f-115">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="da23f-115">-Name</span></span>
<span data-ttu-id="da23f-116">Określa nazwę magazynu, który ma zostać utworzony.</span><span class="sxs-lookup"><span data-stu-id="da23f-116">Specifies the name of the vault to create.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="da23f-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="da23f-117">-ResourceGroupName</span></span>
<span data-ttu-id="da23f-118">Określa nazwę grupy zasobów platformy Azure, w której należy utworzyć lub z której ma zostać pobrany określony obiekt usług Recovery Services.</span><span class="sxs-lookup"><span data-stu-id="da23f-118">Specifies the name of the Azure resource group in which to create or from which to retrieve the specified Recovery Services object.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="da23f-119">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="da23f-119">-Confirm</span></span>
<span data-ttu-id="da23f-120">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="da23f-120">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="da23f-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="da23f-121">-WhatIf</span></span>
<span data-ttu-id="da23f-122">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="da23f-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="da23f-123">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="da23f-123">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="da23f-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="da23f-124">CommonParameters</span></span>
<span data-ttu-id="da23f-125">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="da23f-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="da23f-126">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="da23f-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="da23f-127">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="da23f-127">INPUTS</span></span>

### <span data-ttu-id="da23f-128">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="da23f-128">None</span></span>

## <span data-ttu-id="da23f-129">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="da23f-129">OUTPUTS</span></span>

### <span data-ttu-id="da23f-130">Microsoft. Azure. Commands. RecoveryServices. ARSVault</span><span class="sxs-lookup"><span data-stu-id="da23f-130">Microsoft.Azure.Commands.RecoveryServices.ARSVault</span></span>

## <span data-ttu-id="da23f-131">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="da23f-131">NOTES</span></span>

## <span data-ttu-id="da23f-132">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="da23f-132">RELATED LINKS</span></span>

[<span data-ttu-id="da23f-133">Get-AzRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="da23f-133">Get-AzRecoveryServicesVault</span></span>](./Get-AzRecoveryServicesVault.md)

[<span data-ttu-id="da23f-134">Get-AzRecoveryServicesVaultSettingsFile</span><span class="sxs-lookup"><span data-stu-id="da23f-134">Get-AzRecoveryServicesVaultSettingsFile</span></span>](./Get-AzRecoveryServicesVaultSettingsFile.md)

[<span data-ttu-id="da23f-135">Remove-AzRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="da23f-135">Remove-AzRecoveryServicesVault</span></span>](./Remove-AzRecoveryServicesVault.md)


