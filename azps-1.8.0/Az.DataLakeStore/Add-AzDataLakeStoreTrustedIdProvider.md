---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: 5C788778-58A4-4798-AB66-1D3562BB9338
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/add-azdatalakestoretrustedidprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Add-AzDataLakeStoreTrustedIdProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Add-AzDataLakeStoreTrustedIdProvider.md
ms.openlocfilehash: dc315e2ee69fbccd12ed1f07057e51dab30c04e0
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93868568"
---
# <span data-ttu-id="34c2b-101">Add-AzDataLakeStoreTrustedIdProvider</span><span class="sxs-lookup"><span data-stu-id="34c2b-101">Add-AzDataLakeStoreTrustedIdProvider</span></span>

## <span data-ttu-id="34c2b-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="34c2b-102">SYNOPSIS</span></span>
<span data-ttu-id="34c2b-103">Dodaje zaufanego dostawcę tożsamości do określonego konta usługi Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="34c2b-103">Adds a trusted identity provider to the specified Data Lake Store account.</span></span>

## <span data-ttu-id="34c2b-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="34c2b-104">SYNTAX</span></span>

```
Add-AzDataLakeStoreTrustedIdProvider [-Account] <String> [-Name] <String> [-ProviderEndpoint] <String>
 [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="34c2b-105">Opis</span><span class="sxs-lookup"><span data-stu-id="34c2b-105">DESCRIPTION</span></span>
<span data-ttu-id="34c2b-106">Polecenie cmdlet **Add-AzDataLakeStoreTrustedIdProvider** umożliwia dodanie zaufanego dostawcy tożsamości do określonego konta usługi Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="34c2b-106">The **Add-AzDataLakeStoreTrustedIdProvider** cmdlet adds a trusted identity provider to the specified Data Lake Store account.</span></span>

## <span data-ttu-id="34c2b-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="34c2b-107">EXAMPLES</span></span>

### <span data-ttu-id="34c2b-108">Przykład 1. Dodaj zaufanego dostawcę tożsamości</span><span class="sxs-lookup"><span data-stu-id="34c2b-108">Example 1: Add a trusted identity provider</span></span>
```
PS C:\> Add-AzDataLakeStoreTrustedIdProvider -AccountName "ContosoADL" -Name MyProvider -ProviderEndpoint "https://sts.windows.net/6b04908c-b91f-40ce-8024-7ee8a4fd6150"
```

<span data-ttu-id="34c2b-109">Dodaje dostawcę "The dostarczającego" do konta "ContosoADL" z punktem końcowym dostawcy " https://sts.windows.net/6b04908c-b91f-40ce-8024-7ee8a4fd6150 "</span><span class="sxs-lookup"><span data-stu-id="34c2b-109">Adds the provider "MyProvider" to account "ContosoADL" with the provider endpoint "https://sts.windows.net/6b04908c-b91f-40ce-8024-7ee8a4fd6150"</span></span>

## <span data-ttu-id="34c2b-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="34c2b-110">PARAMETERS</span></span>

### <span data-ttu-id="34c2b-111">— Konto</span><span class="sxs-lookup"><span data-stu-id="34c2b-111">-Account</span></span>
<span data-ttu-id="34c2b-112">Nazwa konta usługi Data Lake Store, do którego ma zostać dodany określony zaufany dostawca tożsamości.</span><span class="sxs-lookup"><span data-stu-id="34c2b-112">The name of the Data Lake Store account to add the specified trusted identity provider to.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AccountName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="34c2b-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="34c2b-113">-DefaultProfile</span></span>
<span data-ttu-id="34c2b-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="34c2b-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="34c2b-115">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="34c2b-115">-Name</span></span>
<span data-ttu-id="34c2b-116">Nazwa zaufanego dostawcy tożsamości, który ma zostać dodany</span><span class="sxs-lookup"><span data-stu-id="34c2b-116">The name of the trusted identity provider to add</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="34c2b-117">-ProviderEndpoint</span><span class="sxs-lookup"><span data-stu-id="34c2b-117">-ProviderEndpoint</span></span>
<span data-ttu-id="34c2b-118">Prawidłowy punkt końcowy zaufanego dostawcy w formacie: https://sts.windows.net/\<provider tożsamość \></span><span class="sxs-lookup"><span data-stu-id="34c2b-118">The valid trusted provider endpoint in the format: https://sts.windows.net/\<provider identity\>"</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="34c2b-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="34c2b-119">-ResourceGroupName</span></span>
<span data-ttu-id="34c2b-120">Nazwa grupy zasobów, pod którą konto ma dodać zaufanego dostawcę tożsamości.</span><span class="sxs-lookup"><span data-stu-id="34c2b-120">Name of resource group under which the account to add the trusted identity provider is.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="34c2b-121">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="34c2b-121">-Confirm</span></span>
<span data-ttu-id="34c2b-122">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="34c2b-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="34c2b-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="34c2b-123">-WhatIf</span></span>
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

### <span data-ttu-id="34c2b-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="34c2b-124">CommonParameters</span></span>
<span data-ttu-id="34c2b-125">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="34c2b-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="34c2b-126">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="34c2b-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="34c2b-127">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="34c2b-127">INPUTS</span></span>

### <span data-ttu-id="34c2b-128">System. String</span><span class="sxs-lookup"><span data-stu-id="34c2b-128">System.String</span></span>

## <span data-ttu-id="34c2b-129">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="34c2b-129">OUTPUTS</span></span>

### <span data-ttu-id="34c2b-130">Microsoft. Azure. Commands. DataLakeStore. models. DataLakeStoreTrustedIdProvider</span><span class="sxs-lookup"><span data-stu-id="34c2b-130">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreTrustedIdProvider</span></span>

## <span data-ttu-id="34c2b-131">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="34c2b-131">NOTES</span></span>

## <span data-ttu-id="34c2b-132">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="34c2b-132">RELATED LINKS</span></span>
