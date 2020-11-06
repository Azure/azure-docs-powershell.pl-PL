---
external help file: Microsoft.Azure.Commands.RecoveryServices.ARM.dll-Help.xml
Module Name: AzureRM.RecoveryServices
ms.assetid: 818B5302-91EE-425F-B1CD-86B626F1B7A3
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices/get-azurermrecoveryservicesvault
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices/help/Get-AzureRmRecoveryServicesVault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices/help/Get-AzureRmRecoveryServicesVault.md
ms.openlocfilehash: bbc059751ee4713b59f6b915efe32bdf57419be2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93550607"
---
# <span data-ttu-id="e9379-101">Get-AzureRmRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="e9379-101">Get-AzureRmRecoveryServicesVault</span></span>

## <span data-ttu-id="e9379-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="e9379-102">SYNOPSIS</span></span>
<span data-ttu-id="e9379-103">Pobiera listę magazynów usług odzyskiwania.</span><span class="sxs-lookup"><span data-stu-id="e9379-103">Gets a list of Recovery Services vaults.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e9379-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="e9379-104">SYNTAX</span></span>

```
Get-AzureRmRecoveryServicesVault [-ResourceGroupName <String>] [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e9379-105">Opis</span><span class="sxs-lookup"><span data-stu-id="e9379-105">DESCRIPTION</span></span>
<span data-ttu-id="e9379-106">Polecenie cmdlet **Get-AzureRmRecoveryServicesVault** pobiera listę magazynów usług odzyskiwania w bieżącej subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="e9379-106">The **Get-AzureRmRecoveryServicesVault** cmdlet gets a list of Recovery Services vaults in the current subscription.</span></span>

## <span data-ttu-id="e9379-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="e9379-107">EXAMPLES</span></span>

### <span data-ttu-id="e9379-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="e9379-108">Example 1</span></span>
```
PS C:\> Get-AzureRmRecoveryServicesVault
```

<span data-ttu-id="e9379-109">Pobierz listę magazynów w wybranej subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="e9379-109">Get the list of vault in selected subscription.</span></span>

### <span data-ttu-id="e9379-110">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="e9379-110">Example 2</span></span>
```
PS C:\> Get-AzureRmRecoveryServicesVault -ResourceGroupName "resourceGroup"
```

<span data-ttu-id="e9379-111">Pobierz listę magazynów w grupie zasób w wybranej subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="e9379-111">Get the list of vault in resource group in selected subscription.</span></span>

### <span data-ttu-id="e9379-112">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="e9379-112">Example 3</span></span>
```
PS C:\> Get-AzureRmRecoveryServicesVault -ResourceGroupName "resourceGroup" -Name "vaultName"
```

<span data-ttu-id="e9379-113">Pobierz magazyn w grupie zasobów o podanej nazwie.</span><span class="sxs-lookup"><span data-stu-id="e9379-113">Get the vault in resource group with given name.</span></span>

## <span data-ttu-id="e9379-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="e9379-114">PARAMETERS</span></span>

### <span data-ttu-id="e9379-115">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="e9379-115">-Name</span></span>
<span data-ttu-id="e9379-116">Określa nazwę magazynu, którego ma dotyczyć kwerenda.</span><span class="sxs-lookup"><span data-stu-id="e9379-116">Specifies the name of the vault to query for.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e9379-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e9379-117">-ResourceGroupName</span></span>
<span data-ttu-id="e9379-118">Określa nazwę grupy zasobów platformy Azure, w której należy utworzyć lub z której ma zostać pobrany określony obiekt usług Recovery Services.</span><span class="sxs-lookup"><span data-stu-id="e9379-118">Specifies the name of the Azure resource group in which to create or from which to retrieve the specified Recovery Services object.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e9379-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e9379-119">-DefaultProfile</span></span>
<span data-ttu-id="e9379-120">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="e9379-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e9379-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e9379-121">CommonParameters</span></span>
<span data-ttu-id="e9379-122">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e9379-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e9379-123">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e9379-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e9379-124">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e9379-124">INPUTS</span></span>

### <span data-ttu-id="e9379-125">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="e9379-125">None</span></span>
<span data-ttu-id="e9379-126">To polecenie cmdlet nie akceptuje żadnych danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="e9379-126">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="e9379-127">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="e9379-127">OUTPUTS</span></span>

### <span data-ttu-id="e9379-128">System. Collections. Generic. list "1 [Microsoft. Azure. Commands. RecoveryServices. ARSVault]</span><span class="sxs-lookup"><span data-stu-id="e9379-128">System.Collections.Generic.List\`1[Microsoft.Azure.Commands.RecoveryServices.ARSVault]</span></span>

## <span data-ttu-id="e9379-129">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="e9379-129">NOTES</span></span>

## <span data-ttu-id="e9379-130">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="e9379-130">RELATED LINKS</span></span>

[<span data-ttu-id="e9379-131">Get-AzureRmRecoveryServicesVaultSettingsFile</span><span class="sxs-lookup"><span data-stu-id="e9379-131">Get-AzureRmRecoveryServicesVaultSettingsFile</span></span>](./Get-AzureRmRecoveryServicesVaultSettingsFile.md)

[<span data-ttu-id="e9379-132">Nowe — AzureRmRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="e9379-132">New-AzureRmRecoveryServicesVault</span></span>](./New-AzureRmRecoveryServicesVault.md)

[<span data-ttu-id="e9379-133">Remove-AzureRmRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="e9379-133">Remove-AzureRmRecoveryServicesVault</span></span>](./Remove-AzureRmRecoveryServicesVault.md)


