---
external help file: Microsoft.Azure.Commands.DataLakeStore.dll-Help.xml
Module Name: AzureRM.DataLakeStore
ms.assetid: 5C788778-58A4-4798-AB66-1D3562BB9338
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakestore/add-azurermdatalakestoretrustedidprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Add-AzureRmDataLakeStoreTrustedIdProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Add-AzureRmDataLakeStoreTrustedIdProvider.md
ms.openlocfilehash: 302ad6ac14ad9fcb08053e70afb7951e72c6e027
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93545752"
---
# <span data-ttu-id="40d67-101">Add-AzureRmDataLakeStoreTrustedIdProvider</span><span class="sxs-lookup"><span data-stu-id="40d67-101">Add-AzureRmDataLakeStoreTrustedIdProvider</span></span>

## <span data-ttu-id="40d67-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="40d67-102">SYNOPSIS</span></span>
<span data-ttu-id="40d67-103">Dodaje zaufanego dostawcę tożsamości do określonego konta usługi Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="40d67-103">Adds a trusted identity provider to the specified Data Lake Store account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="40d67-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="40d67-104">SYNTAX</span></span>

```
Add-AzureRmDataLakeStoreTrustedIdProvider [-Account] <String> [-Name] <String> [-ProviderEndpoint] <String>
 [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="40d67-105">Opis</span><span class="sxs-lookup"><span data-stu-id="40d67-105">DESCRIPTION</span></span>
<span data-ttu-id="40d67-106">Polecenie cmdlet **Add-AzureRmDataLakeStoreTrustedIdProvider** umożliwia dodanie zaufanego dostawcy tożsamości do określonego konta usługi Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="40d67-106">The **Add-AzureRmDataLakeStoreTrustedIdProvider** cmdlet adds a trusted identity provider to the specified Data Lake Store account.</span></span>

## <span data-ttu-id="40d67-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="40d67-107">EXAMPLES</span></span>

### <span data-ttu-id="40d67-108">Przykład 1. Dodaj zaufanego dostawcę tożsamości</span><span class="sxs-lookup"><span data-stu-id="40d67-108">Example 1: Add a trusted identity provider</span></span>
```
PS C:\> Add-AzureRmDataLakeStoreTrustedIdProvider -AccountName "ContosoADL" -Name MyProvider -ProviderEndpoint "https://sts.windows.net/6b04908c-b91f-40ce-8024-7ee8a4fd6150"
```

<span data-ttu-id="40d67-109">Dodaje dostawcę "The dostarczającego" do konta "ContosoADL" z punktem końcowym dostawcy " https://sts.windows.net/6b04908c-b91f-40ce-8024-7ee8a4fd6150 "</span><span class="sxs-lookup"><span data-stu-id="40d67-109">Adds the provider "MyProvider" to account "ContosoADL" with the provider endpoint "https://sts.windows.net/6b04908c-b91f-40ce-8024-7ee8a4fd6150"</span></span>

## <span data-ttu-id="40d67-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="40d67-110">PARAMETERS</span></span>

### <span data-ttu-id="40d67-111">— Konto</span><span class="sxs-lookup"><span data-stu-id="40d67-111">-Account</span></span>
<span data-ttu-id="40d67-112">Nazwa konta usługi Data Lake Store, do którego ma zostać dodany określony zaufany dostawca tożsamości.</span><span class="sxs-lookup"><span data-stu-id="40d67-112">The name of the Data Lake Store account to add the specified trusted identity provider to.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: AccountName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="40d67-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="40d67-113">-DefaultProfile</span></span>
<span data-ttu-id="40d67-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="40d67-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="40d67-115">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="40d67-115">-Name</span></span>
<span data-ttu-id="40d67-116">Nazwa zaufanego dostawcy tożsamości, który ma zostać dodany</span><span class="sxs-lookup"><span data-stu-id="40d67-116">The name of the trusted identity provider to add</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="40d67-117">-ProviderEndpoint</span><span class="sxs-lookup"><span data-stu-id="40d67-117">-ProviderEndpoint</span></span>
<span data-ttu-id="40d67-118">Prawidłowy punkt końcowy zaufanego dostawcy w formacie: https://sts.windows.net/ \<provider identity\> "</span><span class="sxs-lookup"><span data-stu-id="40d67-118">The valid trusted provider endpoint in the format: https://sts.windows.net/\<provider identity\>"</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="40d67-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="40d67-119">-ResourceGroupName</span></span>
<span data-ttu-id="40d67-120">Nazwa grupy zasobów, pod którą konto ma dodać zaufanego dostawcę tożsamości.</span><span class="sxs-lookup"><span data-stu-id="40d67-120">Name of resource group under which the account to add the trusted identity provider is.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="40d67-121">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="40d67-121">-Confirm</span></span>
<span data-ttu-id="40d67-122">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="40d67-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="40d67-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="40d67-123">-WhatIf</span></span>
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

### <span data-ttu-id="40d67-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="40d67-124">CommonParameters</span></span>
<span data-ttu-id="40d67-125">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="40d67-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="40d67-126">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="40d67-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="40d67-127">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="40d67-127">INPUTS</span></span>

### <span data-ttu-id="40d67-128">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="40d67-128">None</span></span>
<span data-ttu-id="40d67-129">To polecenie cmdlet nie akceptuje żadnych danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="40d67-129">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="40d67-130">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="40d67-130">OUTPUTS</span></span>

### <span data-ttu-id="40d67-131">DataLakeStoreTrustedIdProvider</span><span class="sxs-lookup"><span data-stu-id="40d67-131">DataLakeStoreTrustedIdProvider</span></span>
<span data-ttu-id="40d67-132">Dodany dostawca zaufanej tożsamości.</span><span class="sxs-lookup"><span data-stu-id="40d67-132">The added Trusted Identity Provider.</span></span>

## <span data-ttu-id="40d67-133">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="40d67-133">NOTES</span></span>

## <span data-ttu-id="40d67-134">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="40d67-134">RELATED LINKS</span></span>

