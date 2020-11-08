---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: 818B5302-91EE-425F-B1CD-86B626F1B7A3
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesvault
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesVault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesVault.md
ms.openlocfilehash: fcedf52f75b73cc35b7f0e4fd0856600bca6fc71
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94221686"
---
# <span data-ttu-id="a936a-101">Get-AzRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="a936a-101">Get-AzRecoveryServicesVault</span></span>

## <span data-ttu-id="a936a-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="a936a-102">SYNOPSIS</span></span>

<span data-ttu-id="a936a-103">Pobiera listę magazynów usług odzyskiwania.</span><span class="sxs-lookup"><span data-stu-id="a936a-103">Gets a list of Recovery Services vaults.</span></span>

## <span data-ttu-id="a936a-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="a936a-104">SYNTAX</span></span>

### <span data-ttu-id="a936a-105">ByTagNameValueParameterSet</span><span class="sxs-lookup"><span data-stu-id="a936a-105">ByTagNameValueParameterSet</span></span>
```
Get-AzRecoveryServicesVault [[-ResourceGroupName] <String>] [[-Name] <String>] [-TagName <String>]
 [-TagValue <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a936a-106">ByTagObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="a936a-106">ByTagObjectParameterSet</span></span>
```
Get-AzRecoveryServicesVault [[-ResourceGroupName] <String>] [[-Name] <String>] -Tag <Hashtable>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a936a-107">Opis</span><span class="sxs-lookup"><span data-stu-id="a936a-107">DESCRIPTION</span></span>

<span data-ttu-id="a936a-108">Polecenie cmdlet **Get-AzRecoveryServicesVault** pobiera listę magazynów usług odzyskiwania w bieżącej subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="a936a-108">The **Get-AzRecoveryServicesVault** cmdlet gets a list of Recovery Services vaults in the current subscription.</span></span>

## <span data-ttu-id="a936a-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="a936a-109">EXAMPLES</span></span>

### <span data-ttu-id="a936a-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="a936a-110">Example 1</span></span>

```powershell
PS C:\> Get-AzRecoveryServicesVault
```

<span data-ttu-id="a936a-111">Pobierz listę magazynów w wybranej subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="a936a-111">Get the list of vault in selected subscription.</span></span>

### <span data-ttu-id="a936a-112">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="a936a-112">Example 2</span></span>

```powershell
PS C:\> Get-AzRecoveryServicesVault -ResourceGroupName "resourceGroup"
```

<span data-ttu-id="a936a-113">Pobierz listę magazynów w grupie zasób w wybranej subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="a936a-113">Get the list of vault in resource group in selected subscription.</span></span>

### <span data-ttu-id="a936a-114">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="a936a-114">Example 3</span></span>

```powershell
PS C:\> Get-AzRecoveryServicesVault -ResourceGroupName "resourceGroup" -Name "vaultName"
```

<span data-ttu-id="a936a-115">Pobierz magazyn w grupie zasobów o podanej nazwie.</span><span class="sxs-lookup"><span data-stu-id="a936a-115">Get the vault in resource group with given name.</span></span>

## <span data-ttu-id="a936a-116">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="a936a-116">PARAMETERS</span></span>

### <span data-ttu-id="a936a-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a936a-117">-DefaultProfile</span></span>

<span data-ttu-id="a936a-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="a936a-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a936a-119">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="a936a-119">-Name</span></span>

<span data-ttu-id="a936a-120">Określa nazwę magazynu, którego ma dotyczyć kwerenda.</span><span class="sxs-lookup"><span data-stu-id="a936a-120">Specifies the name of the vault to query for.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a936a-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a936a-121">-ResourceGroupName</span></span>

<span data-ttu-id="a936a-122">Określa nazwę grupy zasobów platformy Azure, z której ma zostać pobrany określony obiekt usług Recovery Services.</span><span class="sxs-lookup"><span data-stu-id="a936a-122">Specifies the name of the Azure resource group from which to retrieve the specified Recovery Services object.</span></span>

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

### <span data-ttu-id="a936a-123">-Tag</span><span class="sxs-lookup"><span data-stu-id="a936a-123">-Tag</span></span>

<span data-ttu-id="a936a-124">Określa Tagi do zbadania</span><span class="sxs-lookup"><span data-stu-id="a936a-124">Specifies the Tags to query for</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: ByTagObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a936a-125">-TagName</span><span class="sxs-lookup"><span data-stu-id="a936a-125">-TagName</span></span>

<span data-ttu-id="a936a-126">Określa klucz znacznika, dla którego ma zostać wyszukiwana kwerenda.</span><span class="sxs-lookup"><span data-stu-id="a936a-126">Specifies the Key of the Tag to query for</span></span>

```yaml
Type: System.String
Parameter Sets: ByTagNameValueParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a936a-127">-TagValue</span><span class="sxs-lookup"><span data-stu-id="a936a-127">-TagValue</span></span>

<span data-ttu-id="a936a-128">Określa wartość tagu, dla którego ma zostać wyszukiwana kwerenda.</span><span class="sxs-lookup"><span data-stu-id="a936a-128">Specifies the Value of the Tag to query for</span></span>

```yaml
Type: System.String
Parameter Sets: ByTagNameValueParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a936a-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a936a-129">CommonParameters</span></span>
<span data-ttu-id="a936a-130">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a936a-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a936a-131">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a936a-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a936a-132">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a936a-132">INPUTS</span></span>

### <span data-ttu-id="a936a-133">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="a936a-133">None</span></span>

## <span data-ttu-id="a936a-134">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="a936a-134">OUTPUTS</span></span>

### <span data-ttu-id="a936a-135">Microsoft. Azure. Commands. RecoveryServices. ARSVault</span><span class="sxs-lookup"><span data-stu-id="a936a-135">Microsoft.Azure.Commands.RecoveryServices.ARSVault</span></span>

## <span data-ttu-id="a936a-136">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="a936a-136">NOTES</span></span>
<span data-ttu-id="a936a-137">Get-AzRecoveryServicesVault w starej wersji AZ. RecoveryServices (<= 2.10.0) nie może działać z usługą AZ. accounts (>= 1.8.1) ze względu na niepoprawne odwołanie do zestawu.</span><span class="sxs-lookup"><span data-stu-id="a936a-137">Get-AzRecoveryServicesVault in old version of Az.RecoveryServices(<=2.10.0) cannot work with Az.Accounts(>=1.8.1) because of incorrect assembly reference.</span></span> <span data-ttu-id="a936a-138">Moduł AZ. RecoveryServices musi zostać uaktualniony do 2.11.0 lub nowszego, jeśli używasz najnowszych lub AZ. kont.</span><span class="sxs-lookup"><span data-stu-id="a936a-138">The module Az.RecoveryServices needs to be upgraded to 2.11.0 or newer if you are using the latest Az or Az.Accounts.</span></span>

## <span data-ttu-id="a936a-139">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="a936a-139">RELATED LINKS</span></span>

[<span data-ttu-id="a936a-140">Get-AzRecoveryServicesVaultSettingsFile</span><span class="sxs-lookup"><span data-stu-id="a936a-140">Get-AzRecoveryServicesVaultSettingsFile</span></span>](./Get-AzRecoveryServicesVaultSettingsFile.md)

[<span data-ttu-id="a936a-141">Nowe — AzRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="a936a-141">New-AzRecoveryServicesVault</span></span>](./New-AzRecoveryServicesVault.md)

[<span data-ttu-id="a936a-142">Remove-AzRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="a936a-142">Remove-AzRecoveryServicesVault</span></span>](./Remove-AzRecoveryServicesVault.md)
